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

# ITextRange::GetEnd


## -description


Gets the end character position of the range.


## -parameters




### -param pcpLim

Type: <b>long*</b>

The end character position. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pcpLim</i> is null, the method fails and it returns E_INVALIDARG.




## -remarks



Although a pointer to a range remains valid when the text is edited, this is not the case for the 
				character position. A 
				character position is volatile; that is, it becomes invalid as soon as text is inserted or deleted before the 
				character position. Be careful about using methods that return 
				character position values, especially if the values are to be stored for any duration. 

This method is similar to the <a href="https://msdn.microsoft.com/55c6785f-1e56-4e9d-86bb-d6f963c693b5">ITextRange::GetStart</a> method which gets the start character position of the range.
			




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/55c6785f-1e56-4e9d-86bb-d6f963c693b5">GetStart</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/d84f9fd8-ac3c-4b26-a745-7528c7ba0bb3">SetEnd</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

