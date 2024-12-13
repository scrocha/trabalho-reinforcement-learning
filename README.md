# Trabalho final de Reinforcement Learning

## Em models temos uma estrutura baseada em:

1. Coders:
    - read_data(data, prompt) -> (cleaned_data, used_code)
    - improvement(data, improve_prompt, used_prompt, used_code) -> (cleaned_data, result_code)

2. Reviwer:
    - evaluation(cleaned_data, used_code, score) -> new_prompt
    - make_report(report_prompt, prompt_1, score_1, prompt_2, score_2) -> report

3. Judge:
    - evaluation(report) -> (score)

4. Enviorment:
    - gen_codes(data, prompt_1, prompt_2) -> (cleaned_data_1, code_1, cleaned_data_2, code_2)
    - score(cleaned_data) -> score

    - make_evaluation(cleaned_data, used_code, score) -> new_prompt

    - train_code(initial_prompt_c1, initial_prompt_c2, initial_prompt_r, n_iterations) -> (report, score_loss)

    - train(
        initial_prompt_c1,
        initial_prompt_c2,
        initial_prompt_r,
        report_prompt,
        n_iterations_code,
        n_iterations_report) -> (report, score_report, score_loss_coders)

