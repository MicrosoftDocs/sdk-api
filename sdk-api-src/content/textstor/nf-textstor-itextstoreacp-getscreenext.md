---
UID: NF:textstor.ITextStoreACP.GetScreenExt
title: ITextStoreACP::GetScreenExt (textstor.h)
description: The ITextStoreACP::GetScreenExt method returns the bounding box screen coordinates of the display surface where the text stream is rendered.
helpviewer_keywords: ["GetScreenExt","GetScreenExt method [Text Services Framework]","GetScreenExt method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","GetScreenExt method","ITextStoreACP.GetScreenExt","ITextStoreACP::GetScreenExt","_tsf_itextstoreacp_getscreenext_ref","textstor/ITextStoreACP::GetScreenExt","tsf.itextstoreacp_getscreenext"]
old-location: tsf\itextstoreacp_getscreenext.htm
tech.root: TSF
ms.assetid: bd542dd1-79a5-47ec-a563-cd37a8c36b1a
ms.date: 12/05/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetScreenExt method, ITextStoreACP.GetScreenExt, ITextStoreACP::GetScreenExt, _tsf_itextstoreacp_getscreenext_ref, textstor/ITextStoreACP::GetScreenExt, tsf.itextstoreacp_getscreenext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP::GetScreenExt
 - textstor/ITextStoreACP::GetScreenExt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP.GetScreenExt
---

# ITextStoreACP::GetScreenExt


## -description

The <b>ITextStoreACP::GetScreenExt</b> method returns the bounding box screen coordinates of the display surface where the text stream is rendered.

## -parameters

### -param vcView [in]

Specifies the context view.

### -param prc [out]

Receives the bounding box screen coordinates of the display surface of the document.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>vcView</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

If the text is not currently displayed, for example, if the document window is minimized, the <i>prc</i> parameter is set to { 0, 0, 0, 0 }.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getscreenext">ITfContextOwner::GetScreenExt
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getscreenext">ITfContextView::GetScreenExt
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>