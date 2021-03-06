QuickFIX 101
------------

This example quickfix app was presented at the Chicago FinTech Open Source
meetup on 2013-10-16, hosted by Connamara Systems.

It demonstrates how QuickFIX can be used to rapidly develop a workspace in
which to run a trading strategy.  The workspace provides market data and order
routing to the strategy.

We leverage the "executor" example app that is included with QuickFIX to
simulate an order/execution session, and we use a simple market data simulator
(both included here) to drive the strategy with last trade notifications.

See QuickFIX101.pdf for the slides from the presentation.

Prerequisites
-------------

You will need QuickFIX installed in order to build this project.  If you are
using ubuntu, you can use the version that is available in apt:

    sudo apt-get install libquickfix-dev

See http://quickfixengine.org/download to install from source on other
platforms.

Build
-----

The example code builds in the usual way with autotools:

    ./autogen.sh
    ./configure
    make

Run
---

Start the executor:

    ./executor etc/executor.cfg

Start our market data simulator:

    ./mdsim etc/mdsim.cfg

Start our strategy app:

    ./app etc/app.cfg AAPL

