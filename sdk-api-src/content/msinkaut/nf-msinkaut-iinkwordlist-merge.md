---
UID: NF:msinkaut.IInkWordList.Merge
title: IInkWordList::Merge (msinkaut.h)
description: Merges the specified InkWordList object into this word list.
helpviewer_keywords: ["81c013c3-c033-4dc8-a828-95fcc810e608","IInkWordList","IInkWordList interface [Tablet PC]","Merge method","IInkWordList.Merge","IInkWordList::Merge","InkWordList class [Tablet PC]","Merge method","Merge","Merge method [Tablet PC]","Merge method [Tablet PC]","IInkWordList interface","Merge method [Tablet PC]","InkWordList class","msinkaut/IInkWordList::Merge","tablet.inkwordlist_merge"]
old-location: tablet\inkwordlist_merge.htm
tech.root: tablet
ms.assetid: 81c013c3-c033-4dc8-a828-95fcc810e608
ms.date: 12/05/2018
ms.keywords: 81c013c3-c033-4dc8-a828-95fcc810e608, IInkWordList, IInkWordList interface [Tablet PC],Merge method, IInkWordList.Merge, IInkWordList::Merge, InkWordList class [Tablet PC],Merge method, Merge, Merge method [Tablet PC], Merge method [Tablet PC],IInkWordList interface, Merge method [Tablet PC],InkWordList class, msinkaut/IInkWordList::Merge, tablet.inkwordlist_merge
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkWordList::Merge
 - msinkaut/IInkWordList::Merge
dev_langs:
 - c++
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
---

# IInkWordList::Merge


## -description

Merges the specified <a href="/windows/desktop/tablet/inkwordlist-class">InkWordList</a> object into this word list.

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

<a href="../msinkaut/nn-msinkaut-iinkwordlist.md">IInkWordList</a>



<a href="/windows/desktop/tablet/inkwordlist-class">InkWordList Class</a>
