---
UID: NF:textstor.ITextStoreAnchor.GetWnd
title: ITextStoreAnchor::GetWnd (textstor.h)
description: The ITextStoreAnchor::GetWnd method returns the handle to a window that corresponds to the current text stream.
helpviewer_keywords: ["GetWnd","GetWnd method [Text Services Framework]","GetWnd method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetWnd method","ITextStoreAnchor.GetWnd","ITextStoreAnchor::GetWnd","textstor/ITextStoreAnchor::GetWnd","tsf.itextstoreanchor_getwnd"]
old-location: tsf\itextstoreanchor_getwnd.htm
tech.root: TSF
ms.assetid: e77b5218-45e4-4fe1-a41f-1d7b5887ba30
ms.date: 12/05/2018
ms.keywords: GetWnd, GetWnd method [Text Services Framework], GetWnd method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetWnd method, ITextStoreAnchor.GetWnd, ITextStoreAnchor::GetWnd, textstor/ITextStoreAnchor::GetWnd, tsf.itextstoreanchor_getwnd
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
 - ITextStoreAnchor::GetWnd
 - textstor/ITextStoreAnchor::GetWnd
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
 - ITextStoreAnchor.GetWnd
---

# ITextStoreAnchor::GetWnd


## -description

The <b>ITextStoreAnchor::GetWnd</b> method returns the handle to a window that corresponds to the current text stream.

## -parameters

### -param vcView [in]

Specifies the <a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie</a> data type that corresponds to the current document.

### -param phwnd [out]

Receives a pointer to the handle of the window that corresponds to the current document. This parameter can be <b>NULL</b> if the document does not have the corresponding handle to the window.

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
The <b>TsViewCookie</b> data type is invalid.

</td>
</tr>
</table>

## -remarks

A document might not have a corresponding window handle if the document is in memory but not displayed on the screen, or if the document is a windowless control and the control does not recognize the window handle of the owner of the windowless controls. Callers cannot assume that the <i>phwnd</i> parameter will receive a non-<b>NULL</b> value even if the method is successful. Callers can also receive a <b>NULL</b> value for the <i>phwnd</i> parameter.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>