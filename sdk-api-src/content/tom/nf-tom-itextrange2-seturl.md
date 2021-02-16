---
UID: NF:tom.ITextRange2.SetURL
title: ITextRange2::SetURL (tom.h)
description: Sets the text in this range to that of the specified URL.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetURL method","ITextRange2.SetURL","ITextRange2::SetURL","SetURL","SetURL method [Windows Controls]","SetURL method [Windows Controls]","ITextRange2 interface","controls.itextrange2_seturl","tom/ITextRange2::SetURL"]
old-location: controls\itextrange2_seturl.htm
tech.root: Controls
ms.assetid: f8e62056-5177-4c88-99d8-32ca30bc71e5
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetURL method, ITextRange2.SetURL, ITextRange2::SetURL, SetURL, SetURL method [Windows Controls], SetURL method [Windows Controls],ITextRange2 interface, controls.itextrange2_seturl, tom/ITextRange2::SetURL
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
 - ITextRange2::SetURL
 - tom/ITextRange2::SetURL
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
 - ITextRange2.SetURL
---

# ITextRange2::SetURL


## -description

Sets the text in this range to that of the specified URL.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

The text to use as a URL for the selected friendly name.

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

The URL string is not validated. The text it contains must be enclosed in quotes, optionally preceded by the sentinel character 0xFDDF. For example: "http://www.msn.com" or 0xFDDF"http://www.msn.com". The range must be nondegenerate. 

The following actions are possible:
 
<ul>
<li>If part of a link's friendly name is selected, the URL part is replaced with <i>bstr</i>.</li>
<li>If part of a regular URL is selected, it becomes the link's friendly name, with <i>bstr</i> as the URL.</li>
<li>If nonlink text is selected:<ul>
<li>If the text immediately follows a link's friendly name and <i>bstr</i> matches the URL, the text is appended to the friendly name.</li>
<li>Otherwise, the text becomes the friendly name of a link, with <i>bstr</i> as the URL.</li>
</ul>
</li>
</ul>The text range be adjusted to different character positions after calling <b>SetURL</b>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-geturl">ITextRange2::GetURL</a>