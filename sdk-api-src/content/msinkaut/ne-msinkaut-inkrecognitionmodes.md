---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# InkRecognitionModes enumeration


## -description



Specifies  how the recognizer interprets the ink and determines the result string.




## -enum-fields




### -field IRM_None

The recognizer applies no recognition modes.


### -field IRM_WordModeOnly

The recognizer treats the ink as a single word.

For example, if the recognizer context contains to get her, the recognizer returns together.

<div class="alert"><b>Note</b>  Some compound words in the dictionary are treated as single words by recognizers of Latin script. For example, recognizers of Latin script treat "Los Angeles" as a single word if you use the WordMode flag. In addition, certain factoids-such as the Date <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> in English (United Kingdom), English (United States), German, and French-treat some multiple word dates as single words. For example, these recognizers treat "January 21, 2000" as a single word if you use the WordMode flag.</div>
<div> </div>

### -field IRM_Coerce

The recognizer coerces the result based on the factoid that you specified for the context.

For example, if you specified the Telephone factoid and the user enters the word hello, the recognizer may return a random phone number or an empty string. If you do not specify this flag, the recognizer returns hello as the result.


### -field IRM_TopInkBreaksOnly

The recognizer disables multiple segmentation.

This turns off the recognizer's ability to return recognition results based on more than one recognition segment of the ink, where each segment corresponds to a word (in recognizers of Latin script) or a character (in recognizers of East Asian characters).

In other words, the word together always returns alternates based on together being a single word, and the recognizer does not consider that the string might also be "to get her" or some other variation with differing segmentation.

Turning on this flag enhances recognition speed.


### -field IRM_PrefixOk

The recognizer applies partial word recognition.


### -field IRM_LineMode

The recognizer does not emply line breaking inside the recognizer and all of the ink is recognized as one line.


### -field IRM_DisablePersonalization

The recognizer disables oersonalization on the recognizer.


### -field IRM_AutoSpace

The recognizer should automatically determine word breaks between newly written (and recognized) text and the suffix and prefix.

For example, when AutoSpace is enabled and the user inserts bye after the recognized word, good, the recognizer returns bye with no space inserted before it as the recognized text because the compound "goodbye" is a valid word.

If the user inserts world after the recognized word, hello, the recognizer returns world with a space inserted before it as the recognized text to produce the words, hello world. If AutoSpace is disabled, the recognizer returns world with no space.

This flag is used only by recognizers of Latin script.


### -field IRM_Max

For internal use only.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time using the bitwise <b>OR</b> operator. A compilation error occurs if explicit casting is not used.




## -see-also




<a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags Property</a>
 

 

