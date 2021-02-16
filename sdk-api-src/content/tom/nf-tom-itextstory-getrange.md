---
UID: NF:tom.ITextStory.GetRange
title: ITextStory::GetRange (tom.h)
description: Gets a text range object for the story.
helpviewer_keywords: ["GetRange","GetRange method [Windows Controls]","GetRange method [Windows Controls]","ITextStory interface","ITextStory interface [Windows Controls]","GetRange method","ITextStory.GetRange","ITextStory::GetRange","controls.itextstory_getrange","tom/ITextStory::GetRange"]
old-location: controls\itextstory_getrange.htm
tech.root: Controls
ms.assetid: 7cc02056-c431-470a-83ef-99e47123da1e
ms.date: 12/05/2018
ms.keywords: GetRange, GetRange method [Windows Controls], GetRange method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetRange method, ITextStory.GetRange, ITextStory::GetRange, controls.itextstory_getrange, tom/ITextStory::GetRange
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory::GetRange
 - tom/ITextStory::GetRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetRange
---

# ITextStory::GetRange


## -description

Gets a text range object for the story.

## -parameters

### -param cpActive [in]

Type: <b>long</b>

The active end of the range.

### -param cpAnchor [in]

Type: <b>long</b>

The anchor end of the range.

### -param ppRange [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>**</b>

The text range object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>