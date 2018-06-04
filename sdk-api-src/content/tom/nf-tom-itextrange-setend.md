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

# ITextRange::SetEnd


## -description


Sets the end position of the range.


## -parameters




### -param cpLim






#### - cp

Type: <b>long</b>

The new end position. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE. 




## -remarks



If the new end position is less than the start position, this method also sets the start position to  <i>cp</i>; that is, the range becomes an insertion point.

If this range is actually the selection, the end position becomes the active end and, if the display is not frozen, it is scrolled into view.


<a href="https://msdn.microsoft.com/146c335e-de5a-4418-a0af-51febde720eb">ITextRange::SetStart</a> sets the range's start position and <a href="https://msdn.microsoft.com/aad455a2-bcc1-45f8-b376-c9785400c248">ITextRange::SetRange</a> sets both range ends simultaneously. To convert a nondegenerate range, r, into a degenerate one (insertion point) at  the start position, use

<code>r.End = r.Start</code>

Similarly, r.Start = r.End converts r into an insertion point at the end position.

To add 1 to the end position, unless it is at the end of the story, use:

<code>r.End = r.End + 1</code>

This also makes end position the active end, and it can turn a degenerate range into a nondegenerate one. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/eed9c5f1-416d-4604-8a69-50b284454bb0">GetEnd</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/aad455a2-bcc1-45f8-b376-c9785400c248">SetRange</a>



<a href="https://msdn.microsoft.com/146c335e-de5a-4418-a0af-51febde720eb">SetStart</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

