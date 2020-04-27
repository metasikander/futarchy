# futarchy
a tool for a futarchy-based prediction market in a business setting

# project overview and objectives
prediction markets can be a powerful tool for decision-making, and futarchy is a formal way to build them.  
with this project, i hope to make it easy for businesses to access all available information about the current and future state of their organisation.  
when done right, this tool will be both fun and informative for the whole company, and should help everyone make better descisions.

# scope of work
For the POC, we will need to have these in place:
- descisions on what tools and languages to use
- a sceleton framework to build upon
- a simple proof of concept that works well enough to launch tests

# task list
Live kanban here: https://github.com/metasikander/futarchy/projects

# design goals
- ledger
    - log of all transactions of tokens, from issuance to bets
    - tokens
        - used by the bettors on bets
        - is distributed based on rules set by the admins
        - is always distributed fairly amongst all bettors
- accounts
    - anonymous
    - account types:
        - bettors: is given tokens to use on bets
        - oracles: decides on the outcome of the bets, has the power to invalidate bets
        - admins: manages markets, accepts/rejects new bets, decides how tokens are distributed
- markets
    - new bets builder
        - types: boolean, float
        - if accepted publish
        - if rejected put in archive with comment on reason for rejection
    - market builder
        - connect bets together
            - decision tree
            - matrix
            - linked
            - multidimention
        - description for what the market should show/why the bets are connected

# first principles
*what is needed to make a functioning prediction market*
- accounts should be anonymous so that the bettors don't have to worry about their social status or compromising their social signaling
- the bettors compete amongst each other for the highest level of correctness, based on the amount of tokens they are able to win
- the business hosting the platform should give out prices to the best bettors
- the bettors have to be able to claim the prices without revealing what they have been betting on
- the admins should decide on what bets to accept as valid based on the quality of the bets. if they reject a bet it should be available for everyone to see
- anyone should be able to connect bets together in markets

# references
- futarchy: http://mason.gmu.edu/~rhanson/futarchy.html
- bitcoin hivemind: http://bitcoinhivemind.com/papers/