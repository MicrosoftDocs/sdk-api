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

# IInkRecognitionAlternate::GetTextRangeFromStrokes


## -description



Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.




## -parameters




### -param Strokes [in]

The collection of strokes for which to find the containing alternate.


### -param selectionStart [in, out]

The start position of the range of recognized text within the alternate object on which this method was called that matches the smallest alternate that contains the passed-in strokes.


### -param selectionLength [in, out]

When this method returns, contains the length of the text within the range of recognized text of the smallest alternate that contains the passed-in strokes.


## -returns



If successful, returns S_OK; otherwise, returns an HRESULT error code.




## -remarks



Use this method to retrieve the text that corresponds to a specified range of strokes. For example, consider a collection of strokes, "how are you", that was drawn using nine strokes (one for each letter and three for each word). If a collection that consists of the sixth and seventh strokes is passed in, corresponding to characters "e" and "y", the text range returned matches the alternate containing "are you" and the selection start and length matches this substring.




## -see-also




<a href="https://msdn.microsoft.com/25079651-4fcd-4f13-b73f-7d5ffefa871e">GetStrokesFromStrokeRanges Method</a>



<a href="https://msdn.microsoft.com/7dd8fa24-191f-465d-abd2-9a489df0324a">GetStrokesFromTextRange Method</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognition Alternate Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

