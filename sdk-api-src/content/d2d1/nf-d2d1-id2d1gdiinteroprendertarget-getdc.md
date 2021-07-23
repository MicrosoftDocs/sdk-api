---
UID: NF:d2d1.ID2D1GdiInteropRenderTarget.GetDC
title: ID2D1GdiInteropRenderTarget::GetDC (d2d1.h)
description: Retrieves the device context associated with this render target.
helpviewer_keywords: ["GetDC","GetDC method [Direct2D]","GetDC method [Direct2D]","ID2D1GdiInteropRenderTarget interface","ID2D1GdiInteropRenderTarget interface [Direct2D]","GetDC method","ID2D1GdiInteropRenderTarget.GetDC","ID2D1GdiInteropRenderTarget::GetDC","d2d1/ID2D1GdiInteropRenderTarget::GetDC","direct2d.ID2D1GdiInteropRenderTarget_GetDC"]
old-location: direct2d\ID2D1GdiInteropRenderTarget_GetDC.htm
tech.root: Direct2D
ms.assetid: 40797258-84a0-44ee-8b64-04ceb3eb1998
ms.date: 12/05/2018
ms.keywords: GetDC, GetDC method [Direct2D], GetDC method [Direct2D],ID2D1GdiInteropRenderTarget interface, ID2D1GdiInteropRenderTarget interface [Direct2D],GetDC method, ID2D1GdiInteropRenderTarget.GetDC, ID2D1GdiInteropRenderTarget::GetDC, d2d1/ID2D1GdiInteropRenderTarget::GetDC, direct2d.ID2D1GdiInteropRenderTarget_GetDC
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
 - ID2D1GdiInteropRenderTarget::GetDC
 - d2d1/ID2D1GdiInteropRenderTarget::GetDC
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
 - ID2D1GdiInteropRenderTarget.GetDC
---

# ID2D1GdiInteropRenderTarget::GetDC


## -description

Retrieves the device context associated with this render target.

## -parameters

### -param mode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_dc_initialize_mode">D2D1_DC_INITIALIZE_MODE</a></b>

A value that specifies whether the device context should be cleared.

### -param hdc [out]

Type: <b>HDC*</b>

When this method returns, contains the device context associated with this render target. You must allocate storage for this parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Calling this method flushes the render target.

This command can be called only after <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> and before <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a>. 

<div class="alert"><b>Note</b>  In Windows 7 and earlier, you should not call <b>GetDC</b> between <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip</a>/<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip">PopAxisAlignedClip</a> commands or between <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a>/<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>.  However, this restriction does not apply to Windows 8 and later.</div>
<div> </div>

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc">ReleaseDC</a> must be called once for each call to <b>GetDC</b>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget">ID2D1GdiInteropRenderTarget</a>

