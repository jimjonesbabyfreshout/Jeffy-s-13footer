# 13 Feet Ladder

A site similar to [12ft.io](https://12ft.io) but is self hosted and works with websites that 12ft.io doesn't work with.

## What is this?

This is a simple self hosted server that has a simple but powerful interface to block ads, paywalls, and other nonsense. Specially for sites like medium, new york times which have paid articles that you normally cannot read. Now I do want you to support the creators you benefit from but if you just wanna see one single article and move on with your day then this might be helpful

## How does it work?

It pretends to be GoogleBot (Google's web crawler) and gets the same content that google will get. Google gets the whole page so that the content of the article can be indexed properly and this takes advantage of that.

## How do I use it?

### Using Docker

Requirements:
- docker
- docker-compose
First, clone the repo to your machine then run the following commands:

```sh
git clone https://github.com/wasi-master/13ft.git
cd 13ft
docker-compose up
```

The image is also available from [DockerHub](https://hub.docker.com/r/wasimaster/13ft "docker pull wasimaster/13ft") or [ghcr.io](https://github.com/wasi-master/13ft/pkgs/container/13ft "docker pull ghcr.io/wasi-master/13ft:0.2.3") so the command `docker pull wasimaster/13ft` also works.

### Standard Python script

First, make sure you have [python](https://python.org) installed on your machine. Next, clone the git repo. Then go to a terminal (`Command Prompt` on Windows, `Terminal` on Mac) and run the following command:

From the git cloned directory on your computer:

```sh
cd app/
python -m pip install -r requirements.txt
```

If that doesn't work retry but replace `python` with `py`, then try `python3`, then try `py3`

Then run `portable.py`, click [this link](https://realpython.com/run-python-scripts/) for a tutorial on how to run python scripts.

```sh
python portable.py
```

Then follow these simple steps

### Step 1

![step 1 screenshot](screenshots/step-1.png)
Go to the website at the url shown in the console

### Step 2

![step 2 screenshot](screenshots/step-2.png)
Click on the input box

### Step 3

![step 3 screenshot](screenshots/step-3.png)
Paste your desired url

### Step 4

![step 4 screenshot](screenshots/step-4.gif)
Voilà you now have bypassed the paywall and ads

### Alternative method

You can also append the url at the end of the link and it will also work. (e.g if your server is running at `http://127.0.0.1:5000` then you can go to `http://127.0.0.1:5000/https://example.com` and it will read out the contents of `https://example.com`)

This feature is possible thanks to [atcasanova](https://github.com/atcasanova)
