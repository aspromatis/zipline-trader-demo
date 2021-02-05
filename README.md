# Live Trading with Python Zipline-Trader

## Create and set-up a new virtual environment in Conda

Download and install [Anaconda](https://www.anaconda.com/products/individual)

Installing [Zipline-Trader](https://zipline-trader.readthedocs.io/en/latest/index.html#)

Create a new environment in your conda navigator or terminal and use Python version 3.6 given dependencies.  Running it in a fresh environment is critical and I also don't recommend installing any other packages as it might cause dependency issues.

`$ conda create -n ziptrader36 python=3.6`

Activate the new environment.

`$ conda activate ziptrader36`

Installing with git clone [Zipline-Trader git](https://github.com/shlomikushchi/zipline-trader)

`git clone https://github.com/shlomikushchi/zipline-trader.git`

`pip install -e zipline-trader`

## Alpaca Data Bundle

Data is provided for 'free' with an Alpaca account.

The data bundle is defined in this file: zipline/data/bundles/alpaca_api.py and you will execute it to ingest the necessary data to run your algo.  All the parameters (such as dates) are updatable in that file.  In order for the file to work, you will need to set up a alpaca.yaml file in your rood directory containing all your api credenctial.  Read the [documentation](https://zipline-trader.readthedocs.io/en/latest/alpaca-bundle-ingestion.html) for more detail.

Define your ZIPLINE_ROOT in an environment variable (This is where the ingested data will be stored).  It should be something like this:

`$ ZIPLINE_ROOT=~/.zipline`

To run the Data Bundle

`$ python zipline/data/bundles/alpaca_api.py`

Disclaimer - This is just a demo algo and using it 'as is' carries significant financial risk, so don't use it.  All code and content is for educational purposes only and is not financial advice.
