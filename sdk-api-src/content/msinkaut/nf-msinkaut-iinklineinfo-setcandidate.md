---
UID: NF:msinkaut.IInkLineInfo.SetCandidate
title: IInkLineInfo::SetCandidate (msinkaut.h)
author: windows-sdk-content
description: Updates one recognition alternate in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list.
old-location: tablet\iinklineinfo_setcandidate.htm
tech.root: tablet
ms.assetid: 0301706b-6d3e-4fe4-af87-764b1c959707
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 0301706b-6d3e-4fe4-af87-764b1c959707, IInkLineInfo interface [Tablet PC],SetCandidate method, IInkLineInfo.SetCandidate, IInkLineInfo::SetCandidate, SetCandidate, SetCandidate method [Tablet PC], SetCandidate method [Tablet PC],IInkLineInfo interface, msinkaut/IInkLineInfo::SetCandidate, tablet.iinklineinfo_setcandidate
ms.topic: method
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkLineInfo.SetCandidate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkLineInfo::SetCandidate


## -description



Updates one recognition <i>alternate</i> in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list.




## -parameters




### -param nCandidateNum [in]

Zero based index of the alternate list entry to set.


### -param strRecogWord [in]

Pointer to the new alternate text.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>nCandidateNum</i> index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the operation. The recognition result list is not changed.

</td>
</tr>
</table>
 




## -remarks



The <i>candidate</i> list can only be extended by one new entry at a time, at the end of the current list. For example, if the <i>text ink object (tInk)</i> currently has ten recognition results, then setting the <i>nCandidateNum</i> parameter to 10 adds a new result to the text ink object's recognition result list.




## -see-also




<a href="https://msdn.microsoft.com/59005f51-7052-4aef-915d-4c939eecec99">GetCandidate Method</a>



<a href="https://msdn.microsoft.com/58774f49-6af2-4b81-bbd5-709eb694af2d">IInkLineInfo</a>
 

 

