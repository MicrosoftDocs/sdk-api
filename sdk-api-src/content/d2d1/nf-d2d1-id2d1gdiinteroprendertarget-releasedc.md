---
UID: NF:d2d1.ID2D1GdiInteropRenderTarget.ReleaseDC
title: ID2D1GdiInteropRenderTarget::ReleaseDC (d2d1.h)
description: Indicates that drawing with the device context retrieved using the GetDC method is finished.
helpviewer_keywords: ["ID2D1GdiInteropRenderTarget interface [Direct2D]","ReleaseDC method","ID2D1GdiInteropRenderTarget.ReleaseDC","ID2D1GdiInteropRenderTarget::ReleaseDC","ReleaseDC","ReleaseDC method [Direct2D]","ReleaseDC method [Direct2D]","ID2D1GdiInteropRenderTarget interface","d2d1/ID2D1GdiInteropRenderTarget::ReleaseDC","direct2d.ID2D1GdiInteropRenderTarget_ReleaseDC"]
old-location: direct2d\ID2D1GdiInteropRenderTarget_ReleaseDC.htm
tech.root: Direct2D
ms.assetid: 802bd023-f223-4505-9911-95b43f3490e3
ms.date: 12/05/2018
ms.keywords: ID2D1GdiInteropRenderTarget interface [Direct2D],ReleaseDC method, ID2D1GdiInteropRenderTarget.ReleaseDC, ID2D1GdiInteropRenderTarget::ReleaseDC, ReleaseDC, ReleaseDC method [Direct2D], ReleaseDC method [Direct2D],ID2D1GdiInteropRenderTarget interface, d2d1/ID2D1GdiInteropRenderTarget::ReleaseDC, direct2d.ID2D1GdiInteropRenderTarget_ReleaseDC
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GdiInteropRenderTarget::ReleaseDC
 - d2d1/ID2D1GdiInteropRenderTarget::ReleaseDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiInteropRenderTarget.ReleaseDC
---

# ID2D1GdiInteropRenderTarget::ReleaseDC


## -description

Indicates that drawing with the device context retrieved using the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">GetDC</a> method is finished.

## -parameters

### -param update [in, optional]

Type: <b><a href="/windows/win32/api/windef/ns-windef-rect">RECT</a>*</b>

The modified region of the device context, or <b>NULL</b> to specify the entire render target.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

<b>ReleaseDC</b> must be called once for each call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">GetDC</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget">ID2D1GdiInteropRenderTarget</a>

