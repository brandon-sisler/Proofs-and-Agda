Note: This is a ladga.md file. All agda code must be written between ``` ```. 
All other text will be treated as in a markdown file. 

```
module Chapter1-Agda where


module example where 
-- Here you can see that you are allowed to have nested namespaces within agda files 

module Example-Imports where 
    import Data.Bool --Let the user work with the contents of Data.Bool 
    open Data.Bool   --Open the namespace, so Data.Bool.Bool can be refered to as Bool


module Example-TypingJudgements where 
    postulate 
        Bool : Set --Risky, we are forcing an object to exist apart from our knowlege of its constructors
        true : Bool 
        false : Bool 
        -- Nothing stops us from adding more to Bool here. So this should be a last resort
        -- Better to construct Bool as a data type

module Booleans where 
    data Bool : Set where 
        true : Bool 
        false : Bool 
    
    -- Define the not function on the booleans 
    not : Bool → Bool 
    not true = false 
    not false = true 
```