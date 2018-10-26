---
UID: NF:msinkaut.IInkWordList.Merge
title: IInkWordList::Merge
author: windows-sdk-content
description: Merges the specified InkWordList object into this word list.
old-location: tablet\inkwordlist_merge.htm
tech.root: tablet
ms.assetid: 81c013c3-c033-4dc8-a828-95fcc810e608
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 81c013c3-c033-4dc8-a828-95fcc810e608, IInkWordList, IInkWordList interface [Tablet PC],Merge method, IInkWordList.Merge, IInkWordList::Merge, InkWordList class [Tablet PC],Merge method, Merge, Merge method [Tablet PC], Merge method [Tablet PC],IInkWordList interface, Merge method [Tablet PC],InkWordList class, msinkaut/IInkWordList::Merge, tablet.inkwordlist_merge
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkWordList.Merge
 - InkWordList.Merge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkWordList::Merge


## -description



Merges the specified <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a> object into this word list.




## -parameters




### -param MergeWordList [in]

The word list to merge into this word list. Words that already exist in the list are not added.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4E872C5A-1223-48EB-9B7D-04B3ADB84B2B">IInkWordList</a>



<a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList Class</a>
 

 

