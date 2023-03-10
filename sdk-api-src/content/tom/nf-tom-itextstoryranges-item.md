---
UID: NF:tom.ITextStoryRanges.Item
title: ITextStoryRanges::Item (tom.h)
description: Retrieves an ITextRange object for the Indexth story in this story collection.
helpviewer_keywords: ["ITextStoryRanges interface [Windows Controls]","Item method","ITextStoryRanges.Item","ITextStoryRanges::Item","Item","Item method [Windows Controls]","Item method [Windows Controls]","ITextStoryRanges interface","_win32_ITextStoryRanges_Item","_win32_ITextStoryRanges_Item_cpp","controls.ITextStoryRanges_Item","controls._win32_ITextStoryRanges_Item","tom/ITextStoryRanges::Item"]
old-location: controls\ITextStoryRanges_Item.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\item.htm
ms.date: 12/05/2018
ms.keywords: ITextStoryRanges interface [Windows Controls],Item method, ITextStoryRanges.Item, ITextStoryRanges::Item, Item, Item method [Windows Controls], Item method [Windows Controls],ITextStoryRanges interface, _win32_ITextStoryRanges_Item, _win32_ITextStoryRanges_Item_cpp, controls.ITextStoryRanges_Item, controls._win32_ITextStoryRanges_Item, tom/ITextStoryRanges::Item
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoryRanges::Item
 - tom/ITextStoryRanges::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextStoryRanges.Item
---

# ITextStoryRanges::Item


## -description

Retrieves an <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object for the 
			<i>Index</i>th story in this story collection.

## -parameters

### -param Index

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of story range that is retrieved. The default value is 1, which indicates the first story in the collection. <i>Count</i>, given by <a href="/windows/desktop/api/tom/nf-tom-itextstoryranges-getcount">ITextStoryRanges::GetCount</a>, indicates the last story in the collection. If <i>Index</i> is less than zero, the stories are counted from last to first, with -1 being the index of the last story in the collection, and 
					<i>Index</i> = - <i>Count</i> indicating the first story in the collection.

### -param ppRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>**</b>

The <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object.

## -returns

Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
ppRange is null or Index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextstoryranges-getcount">GetCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextstoryranges">ITextStoryRanges</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>