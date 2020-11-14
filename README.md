# FrameSentence

import UIKit

func splitSentence(sentence: [String]){
    
    print("************")
    var element = 0
    let maxWidth = 10
    var space = ""
    
    // This for loop prints each word using a repeat/while loop to calculate the spaces
    for _ in sentence{
        let myElement = (sentence[element])
        let spaceCount = maxWidth - myElement.count
        var neededSpaces = maxWidth - spaceCount
        
        repeat {
            space += " "
        
            neededSpaces += 1

        } while neededSpaces < maxWidth
        
        print("*\(myElement + space)*")
        element += 1
        space = ""
    }
    print("************")
}

splitSentence(sentence: ["This", "is", "a", "frame", "print"])
