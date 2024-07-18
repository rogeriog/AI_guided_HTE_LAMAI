# AI guided High-Throughput Experimentation 
This repository contains tools to perform High-Throughput Experimentation with the aid of state-of-the-art AI tools to design a LARP synthesis from the choice of reactant and ligands for the goal material to specific quantities of each reactant and the complete synthesis protocol to be executed with the liquid handler robot. The repository contains the following folders corresponding to each stage of the project outlining:
1. **autogpt_outlining**: AutoGPT[1] procedure of feeding the results of the LLM actions back into the prompt are applied to outline the research focus employing GPT-4 as implemented in Microsoft's Bing generative AI model[2].
2. **gpt_data_extraction**: upon downloading the suggested papers from the AutoGPT Outlining step to define our research focus, we extracted relevant data to build a database containing important synthesis information such as the type of precursors, ligands and additives as well as their quantities and resulting properties of the nanoparticles (solution stability, size, dispersity and PLQY quality). This extraction is made with either Microsoft's Bing AI model or OpenAI's GPT-4o model[3].
3. **gpt_critical_assessment**: from the given database, GPT-4 model is utilized to critically assess the most promising combinations of reactants and the initial proposed synthesis protocol is updated.
4. **graphical_prognostic_and_protocol**: using a home-made code[4] coupled with the Opentrons API, a graphical prognostic is presented to review the LARP synthesis that was refined through AI. The final protocol is also evaluated by the opentrons_simulate algorithm to verify any incosistencies. 

At the end of this process, all synthesis protocols should be ready to start the high-throughput experiments with the liquid handler robot.

***This work is being conducted in the Laboratory of Applied Materials and Interfaces (LAMAI) from the Institute of Chemistry at Federal University of Rio Grande do Sul (UFRGS) in Brazil.***

[1] Introduction - AutoGPT Documentation. Agpt.co. Published 2024. Accessed July 18, 2024. https://docs.agpt.co/autogpt/ 
[2] Microsoft. (2024). Bing AI (Version 4.0). [Large language model] https://www.bing.com
[3] OpenAI. (2024). ChatGPT (GPT-4o version) [Large language model] https://openai.com/index/hello-gpt-4o/
[4] Opentrons Graphical Prognostic for LARP. https://github.com/rogeriog/opentrons_LARP_graphical_prognostic
‌
