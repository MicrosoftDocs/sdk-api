---
UID: NF:d2d1.ID2D1DCRenderTarget.BindDC
title: ID2D1DCRenderTarget::BindDC (d2d1.h)
description: Binds the render target to the device context to which it issues drawing commands.
helpviewer_keywords: ["BindDC","BindDC method [Direct2D]","BindDC method [Direct2D]","ID2D1DCRenderTarget interface","ID2D1DCRenderTarget interface [Direct2D]","BindDC method","ID2D1DCRenderTarget.BindDC","ID2D1DCRenderTarget::BindDC","d2d1/ID2D1DCRenderTarget::BindDC","direct2d.ID2D1DCRenderTarget_BindDC"]
old-location: direct2d\ID2D1DCRenderTarget_BindDC.htm
tech.root: Direct2D
ms.assetid: a5e98470-9a9f-4a85-b00f-afb2ead3fb31
ms.date: 12/05/2018
ms.keywords: BindDC, BindDC method [Direct2D], BindDC method [Direct2D],ID2D1DCRenderTarget interface, ID2D1DCRenderTarget interface [Direct2D],BindDC method, ID2D1DCRenderTarget.BindDC, ID2D1DCRenderTarget::BindDC, d2d1/ID2D1DCRenderTarget::BindDC, direct2d.ID2D1DCRenderTarget_BindDC
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
 - ID2D1DCRenderTarget::BindDC
 - d2d1/ID2D1DCRenderTarget::BindDC
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
 - ID2D1DCRenderTarget.BindDC
---

# ID2D1DCRenderTarget::BindDC


## -description

Binds the render target to the device context to which it issues drawing commands.

## -parameters

### -param hDC

Type: <b>const HDC</b>

The device context to which the render target issues drawing commands.

### -param pSubRect [in]

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-rect">RECT</a>*</b>

The dimensions of the handle to a device context (HDC) to which the render target is bound.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Before you can render with the DC render target, you must use its <b>BindDC</b> method to associate it with a GDI DC.  You do this each time you  use a different DC, or the size of the area you want to draw to changes.


## Examples

In the preceding code, <i>m_pD2DFactory</i> is a  pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>, and <i>m_pDCRT</i> is a pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>. 

The next code example binds a DC to the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>.


```cpp
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

```

```cpp
// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);

```

```cpp
// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);

```

## -see-also

<a href="/windows/win32/Direct2D/direct2d-and-gdi-interoperation-overview">Direct2D and GDI Interoperation Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>

