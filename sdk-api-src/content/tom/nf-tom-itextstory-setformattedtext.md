---
UID: NF:tom.ITextStory.SetFormattedText
title: ITextStory::SetFormattedText (tom.h)
description: Replaces a story’s text with specified formatted text.
helpviewer_keywords: ["ITextStory interface [Windows Controls]","SetFormattedText method","ITextStory.SetFormattedText","ITextStory::SetFormattedText","SetFormattedText","SetFormattedText method [Windows Controls]","SetFormattedText method [Windows Controls]","ITextStory interface","controls.itextstory_setformattedtext","tom/ITextStory::SetFormattedText"]
old-location: controls\itextstory_setformattedtext.htm
tech.root: Controls
ms.assetid: ddc77bfe-06de-43e6-9d74-f1b3531c9416
ms.date: 12/05/2018
ms.keywords: ITextStory interface [Windows Controls],SetFormattedText method, ITextStory.SetFormattedText, ITextStory::SetFormattedText, SetFormattedText, SetFormattedText method [Windows Controls], SetFormattedText method [Windows Controls],ITextStory interface, controls.itextstory_setformattedtext, tom/ITextStory::SetFormattedText
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
 - ITextStory::SetFormattedText
 - tom/ITextStory::SetFormattedText
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
 - ITextStory.SetFormattedText
---

# ITextStory::SetFormattedText


## -description

Replaces a story’s text with specified formatted text.

## -parameters

### -param pUnk [in]

Type: <b>IUnknown*</b>

The formatted text to replace the story’s text.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

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

## -remarks

This method calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> for an <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> interface.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstory">ITextStory</a>