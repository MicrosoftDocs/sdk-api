---
UID: NF:textserv.ITextServices2.TxDrawD2D
title: ITextServices2::TxDrawD2D (textserv.h)
description: Draws the text services object by using Direct2D rendering.
helpviewer_keywords: ["ITextServices2 interface [Windows Controls]","TxDrawD2D method","ITextServices2.TxDrawD2D","ITextServices2::TxDrawD2D","TXTVIEW_ACTIVE","TXTVIEW_INACTIVE","TxDrawD2D","TxDrawD2D method [Windows Controls]","TxDrawD2D method [Windows Controls]","ITextServices2 interface","controls.itextservices2_txdrawd2d","textserv/ITextServices2::TxDrawD2D"]
old-location: controls\itextservices2_txdrawd2d.htm
tech.root: Controls
ms.assetid: B45B015A-0A2C-49DD-9AA9-FC2A530BD057
ms.date: 12/05/2018
ms.keywords: ITextServices2 interface [Windows Controls],TxDrawD2D method, ITextServices2.TxDrawD2D, ITextServices2::TxDrawD2D, TXTVIEW_ACTIVE, TXTVIEW_INACTIVE, TxDrawD2D, TxDrawD2D method [Windows Controls], TxDrawD2D method [Windows Controls],ITextServices2 interface, controls.itextservices2_txdrawd2d, textserv/ITextServices2::TxDrawD2D
req.header: textserv.h
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
 - ITextServices2::TxDrawD2D
 - textserv/ITextServices2::TxDrawD2D
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
 - ITextServices2.TxDrawD2D
---

# ITextServices2::TxDrawD2D


## -description

Draws the text services object by using Direct2D rendering.

## -parameters

### -param pRenderTarget

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>*</b>

The Direct2D rendering object that draws the text services object.

### -param lprcBounds

Type: <b><a href="/windows/win32/api/windef/ns-windef-rectl">LPCRECTL</a></b>

The bounding (client) rectangle.

### -param lprcUpdate

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">LPRECT</a></b>

The rectangle to update inside <i>lprcBounds</i> rectangle, in the logical coordinate system of drawing device context. If this parameter is NULL, the entire client rectangle should be drawn.

### -param lViewId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The view to draw.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_ACTIVE"></a><a id="txtview_active"></a><dl>
<dt><b>TXTVIEW_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw the in-place   active view.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_INACTIVE"></a><a id="txtview_inactive"></a><dl>
<dt><b>TXTVIEW_INACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw a view other than the in-place active view, for example, a print    preview. 

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itextservices2">ITextServices2</a>