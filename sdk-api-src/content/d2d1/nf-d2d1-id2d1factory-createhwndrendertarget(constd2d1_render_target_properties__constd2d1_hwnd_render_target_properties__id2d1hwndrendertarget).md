---
UID: NF:d2d1.ID2D1Factory.CreateHwndRenderTarget(constD2D1_RENDER_TARGET_PROPERTIES&,constD2D1_HWND_RENDER_TARGET_PROPERTIES&,ID2D1HwndRenderTarget)
title: ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget) (d2d1.h)
description: Creates an ID2D1HwndRenderTarget, a render target that renders to a window. (overload 2/2)
helpviewer_keywords: ["CreateHwndRenderTarget","CreateHwndRenderTarget method [Direct2D]","CreateHwndRenderTarget method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateHwndRenderTarget method","ID2D1Factory.CreateHwndRenderTarget","ID2D1Factory.CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &","const D2D1_HWND_RENDER_TARGET_PROPERTIES &","ID2D1HwndRenderTarget)","ID2D1Factory::CreateHwndRenderTarget","ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &","const D2D1_HWND_RENDER_TARGET_PROPERTIES &","ID2D1HwndRenderTarget)","d2d1/ID2D1Factory::CreateHwndRenderTarget","direct2d.ID2D1Factory_CreateHwndRenderTarget_ref_D2D1_RENDER_TARGET_PROPERTIES_ref_D2D1_HWND_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1HwndRenderTarget"]
old-location: direct2d\ID2D1Factory_CreateHwndRenderTarget_ref_D2D1_RENDER_TARGET_PROPERTIES_ref_D2D1_HWND_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1HwndRenderTarget.htm
tech.root: Direct2D
ms.assetid: c1f5f5dd-3ae8-4483-bd7d-f25a69489bab
ms.date: 12/05/2018
ms.keywords: CreateHwndRenderTarget, CreateHwndRenderTarget method [Direct2D], CreateHwndRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateHwndRenderTarget method, ID2D1Factory.CreateHwndRenderTarget, ID2D1Factory.CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget), ID2D1Factory::CreateHwndRenderTarget, ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget), d2d1/ID2D1Factory::CreateHwndRenderTarget, direct2d.ID2D1Factory_CreateHwndRenderTarget_ref_D2D1_RENDER_TARGET_PROPERTIES_ref_D2D1_HWND_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1HwndRenderTarget
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1Factory::CreateHwndRenderTarget
 - d2d1/ID2D1Factory::CreateHwndRenderTarget
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
 - ID2D1Factory.CreateHwndRenderTarget
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

When you create a render target, and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a> error is received. When you receive this error, you need to recreate the render target (and any resources it created).

## -parameters

### -param renderTargetProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a> &</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering.  For information about supported pixel formats, see  <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>.

### -param hwndRenderTargetProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties">D2D1_HWND_RENDER_TARGET_PROPERTIES</a> &</b>

The window handle, initial size (in pixels), and present options.

### -param hwndRenderTarget

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> object created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).

## Examples

The following example creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>.

```cpp
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>

