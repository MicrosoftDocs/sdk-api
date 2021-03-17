---
UID: NF:textstor.ITextStoreAnchor.GetScreenExt
title: ITextStoreAnchor::GetScreenExt (textstor.h)
description: The ITextStoreAnchor::GetScreenExt method returns the bounding box screen coordinates of the display surface where the text stream is rendered.
helpviewer_keywords: ["GetScreenExt","GetScreenExt method [Text Services Framework]","GetScreenExt method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetScreenExt method","ITextStoreAnchor.GetScreenExt","ITextStoreAnchor::GetScreenExt","textstor/ITextStoreAnchor::GetScreenExt","tsf.itextstoreanchor_getscreenext"]
old-location: tsf\itextstoreanchor_getscreenext.htm
tech.root: TSF
ms.assetid: 5e1b446e-935f-492a-b168-8d1b60868d72
ms.date: 12/05/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetScreenExt method, ITextStoreAnchor.GetScreenExt, ITextStoreAnchor::GetScreenExt, textstor/ITextStoreAnchor::GetScreenExt, tsf.itextstoreanchor_getscreenext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor::GetScreenExt
 - textstor/ITextStoreAnchor::GetScreenExt
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
 - ITextStoreAnchor.GetScreenExt
---

# ITextStoreAnchor::GetScreenExt


## -description

The <b>ITextStoreAnchor::GetScreenExt</b> method returns the bounding box screen coordinates of the display surface where the text stream is rendered.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getscreenext">ITfContextOwner::GetScreenExt
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getscreenext">ITfContextView::GetScreenExt
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>