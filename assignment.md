# Assignment

## Brief

Write the YML for the following questions.

## Instructions

Paste the answer as YML in the answer code section below each question.

### Question 1

Question: Add 2 more tests each using `dbt_utils` and `dbt-expectations` to `fact_sales`.

Answer:

Specs for `dbt_utils`:

```yml
      #Check for bottles_sold less than '0'. Results: 9760 rows have bottles_sold less than '0'
      - name: bottles_sold
        tests:
          - dbt_utils.accepted_range:
              min_value: 0
```

Specs for `dbt-expectations`:

```yml
      #Check for sale_dollars less than '0'. Results: 9760 rows have sale_dollars less than '0'
      - name: sale_dollars
        tests:
          - dbt_expectations.expect_column_values_to_be_between:
              min_value: 0
```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
