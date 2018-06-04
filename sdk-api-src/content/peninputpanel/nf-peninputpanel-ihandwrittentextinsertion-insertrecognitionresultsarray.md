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

# IHandwrittenTextInsertion::InsertRecognitionResultsArray


## -description



Insert recognition results array.




## -parameters




### -param psaAlternates [in]

A two-dimensional array of strings, where each entry in the first array is a list of alternates for a single word. The first entry in the sub arrays of alternates is the text to insert (the top alternate).


### -param locale [in]

A specific culture for the input language of the recognizer used to produce alternates.


### -param fAlternateContainsAutoSpacingInformation [in]

Specifies whether the recognized text is generated with auto-spacing enabled. When <b>FALSE</b>, a space at the start/end of the lattice will always be inserted. When <b>TRUE</b>, a space exists, and is added where necessary. If no space exists, a space is consumed.


## -returns



This method can return one of these values.




## -remarks



This element is declared in Peninputpanel.h.




## -see-also




<a href="https://msdn.microsoft.com/67fcf19a-a864-40de-987f-406f18726a9f">IHandWrittenTextInsertion</a>
 

 

