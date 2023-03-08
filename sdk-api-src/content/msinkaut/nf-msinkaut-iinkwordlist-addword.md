---
UID: NF:msinkaut.IInkWordList.AddWord
title: IInkWordList::AddWord (msinkaut.h)
description: Adds a single word to the InkWordList object.
helpviewer_keywords: ["AddWord","AddWord method [Tablet PC]","AddWord method [Tablet PC]","IInkWordList interface","AddWord method [Tablet PC]","InkWordList class","IInkWordList","IInkWordList interface [Tablet PC]","AddWord method","IInkWordList.AddWord","IInkWordList::AddWord","InkWordList class [Tablet PC]","AddWord method","bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4","msinkaut/IInkWordList::AddWord","tablet.inkwordlist_addword"]
old-location: tablet\inkwordlist_addword.htm
tech.root: tablet
ms.assetid: bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4
ms.date: 12/05/2018
ms.keywords: AddWord, AddWord method [Tablet PC], AddWord method [Tablet PC],IInkWordList interface, AddWord method [Tablet PC],InkWordList class, IInkWordList, IInkWordList interface [Tablet PC],AddWord method, IInkWordList.AddWord, IInkWordList::AddWord, InkWordList class [Tablet PC],AddWord method, bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4, msinkaut/IInkWordList::AddWord, tablet.inkwordlist_addword
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
 - IInkWordList::AddWord
 - msinkaut/IInkWordList::AddWord
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
 - IInkWordList.AddWord
 - InkWordList.AddWord
---

# IInkWordList::AddWord


## -description

Adds a single word to the <a href="/windows/desktop/tablet/inkwordlist-class">InkWordList</a> object.

## -parameters

### -param NewWord [in]

The word to add to an <a href="/windows/desktop/tablet/inkwordlist-class">InkWordList</a> object. The word is not added if it already exists in the list.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The word already exists in the list.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -remarks

If a string is added to a word list, its capitalized versions are also implicitly added. For instance, adding "hello" implicitly adds "Hello" and "HELLO".

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkwordlist.md">IInkWordList</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/windows/desktop/tablet/inkwordlist-class">InkWordList Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkwordlist-removeword">RemoveWord Method</a>
