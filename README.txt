1. DESCRIPTION
    <Directory Structure>
    flask/
    twint/
        recommendation.py
        web/
            data/ --> "Preprocessed_data.csv" downloaded from Kaggle / "merged_Agedata_final.csv" from the preprocessing step
            lib/
            icon/
            welcome.html
            visualization.html
            selection.html
    
2. INSTALLATION
    (1) <Download Dataset>
        https://www.kaggle.com/ruchi798/bookcrossing-dataset
        ***
        put "Preprocessed_data.csv" under web/data/
        ***

    (2) <Preprocess Dataset>
        Run Age_data_merging.ipynb to get "merged_Agedata_final.csv"
	(Input: BX_Books.csv,BX-Book-Ratings.csv, BX-Users.csv. Filepath in the ipynb need to be defined)
	***
	preprocess.py is used to generate "region_score_sort.csv", "cat_count_sort.csv", "cat_score_sort.csv"
	***

    (3) <Install Flask>
        pip3 install flask
        pip install virtualenv
        virtualenv flask
        cd flask
        source bin/activate

    (4) <Install Twint> Source: https://github.com/twintproject/twint
        git clone --depth=1 https://github.com/twintproject/twint.git
        cd twint
        pip3 install . -r requirements.txt
        pip3 install twint
        
        ***
        put recommendation.py under the twint directory
        put web files under the twint directory
        ***

    (5) <install eel> Source: https://github.com/ChrisKnott/Eel
        pip install eel
    
    (6) <install python package>
        pip install nltk
        pip install sklearn
        pip install matplotlib
    
3. EXECUTION
    Run "python recommendation.py" //under the twint directory
    ***
    error msg: "[IMPORTERROR] cannot import name 'CeilTimeout' from 'aiohttp.helpers'"
    solution: pip install aiohttp==3.7.0
    ***

4. DEMO VIDEO
    https://youtu.be/k9ozAC1UNwg
