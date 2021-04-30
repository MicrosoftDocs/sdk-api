---
UID: NF:tom.ITextRange2.GetURL
title: ITextRange2::GetURL (tom.h)
description: Returns the URL text associated with a range.
helpviewer_keywords: ["GetURL","GetURL method [Windows Controls]","GetURL method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetURL method","ITextRange2.GetURL","ITextRange2::GetURL","controls.itextrange2_geturl","tom/ITextRange2::GetURL"]
old-location: controls\itextrange2_geturl.htm
tech.root: Controls
ms.assetid: 0d23f261-0b44-4532-86da-0ca40561bfe0
ms.date: 12/05/2018
ms.keywords: GetURL, GetURL method [Windows Controls], GetURL method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetURL method, ITextRange2.GetURL, ITextRange2::GetURL, controls.itextrange2_geturl, tom/ITextRange2::GetURL
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextRange2::GetURL
 - tom/ITextRange2::GetURL
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
 - ITextRange2.GetURL
---

# ITextRange2::GetURL


## -description

Returns the URL text associated with a range.

## -parameters

### -param pbstr [out, retval]

Type: <b>BSTR*</b>

The URL text associated with the range.

## -returns

Type: <b>HRESULT</b>

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

## -remarks

This method sets the start and end positions of the range to that of the whole hyperlink, including the friendly name, if any.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-seturl">ITextRange2::SetURL</a>