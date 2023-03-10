---
UID: NF:textstor.ITextStoreACP2.GetScreenExt
title: ITextStoreACP2::GetScreenExt (textstor.h)
description: Gets the bounding box screen coordinates of the display surface where the text stream is rendered.
helpviewer_keywords: ["GetScreenExt","GetScreenExt method [Text Services Framework]","GetScreenExt method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetScreenExt method","ITextStoreACP2.GetScreenExt","ITextStoreACP2::GetScreenExt","textstor/ITextStoreACP2::GetScreenExt","tsf.itextstoreacp2_getscreenext"]
old-location: tsf\itextstoreacp2_getscreenext.htm
tech.root: TSF
ms.assetid: fdc258ab-b692-495c-be76-0b41d75625e2
ms.date: 12/05/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetScreenExt method, ITextStoreACP2.GetScreenExt, ITextStoreACP2::GetScreenExt, textstor/ITextStoreACP2::GetScreenExt, tsf.itextstoreacp2_getscreenext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::GetScreenExt
 - textstor/ITextStoreACP2::GetScreenExt
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
 - ITextStoreACP2.GetScreenExt
---

# ITextStoreACP2::GetScreenExt


## -description

Gets the bounding box screen coordinates of the display surface where the text stream is rendered.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getscreenext">ITfContextOwner::GetScreenExt
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getscreenext">ITfContextView::GetScreenExt
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>