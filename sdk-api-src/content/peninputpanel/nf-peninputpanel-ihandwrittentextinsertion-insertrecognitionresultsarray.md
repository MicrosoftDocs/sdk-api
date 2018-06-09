---
UID: NF:peninputpanel.IHandwrittenTextInsertion.InsertRecognitionResultsArray
title: IHandwrittenTextInsertion::InsertRecognitionResultsArray
author: windows-sdk-content
description: Insert recognition results array.
old-location: tablet\ihandwrittentextinsertion_insertrecognitionresultsarray.htm
old-project: tablet
ms.assetid: c3566d1c-e4fb-4f0d-9beb-0b5e5db66985
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IHandWrittenTextInsertion interface [Tablet PC],InsertRecognitionResultsArray method, IHandWrittenTextInsertion::InsertRecognitionResultsArray, IHandwrittenTextInsertion.InsertRecognitionResultsArray, IHandwrittenTextInsertion::InsertRecognitionResultsArray, InsertRecognitionResultsArray, InsertRecognitionResultsArray method [Tablet PC], InsertRecognitionResultsArray method [Tablet PC],IHandWrittenTextInsertion interface, c3566d1c-e4fb-4f0d-9beb-0b5e5db66985, peninputpanel/IHandWrittenTextInsertion::InsertRecognitionResultsArray, tablet.ihandwrittentextinsertion_insertrecognitionresultsarray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - IHandWrittenTextInsertion.InsertRecognitionResultsArray
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

