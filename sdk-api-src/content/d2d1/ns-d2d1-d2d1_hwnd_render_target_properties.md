---
UID: NS:d2d1.D2D1_HWND_RENDER_TARGET_PROPERTIES
title: D2D1_HWND_RENDER_TARGET_PROPERTIES (d2d1.h)
description: Contains the HWND, pixel size, and presentation options for an ID2D1HwndRenderTarget.
helpviewer_keywords: ["D2D1_HWND_RENDER_TARGET_PROPERTIES","D2D1_HWND_RENDER_TARGET_PROPERTIES structure [Direct2D]","d2d1/D2D1_HWND_RENDER_TARGET_PROPERTIES","direct2d.D2D1_HWND_RENDER_TARGET_PROPERTIES"]
old-location: direct2d\D2D1_HWND_RENDER_TARGET_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 4300843a-a24f-4f9e-a396-67172f083638
ms.date: 12/05/2018
ms.keywords: D2D1_HWND_RENDER_TARGET_PROPERTIES, D2D1_HWND_RENDER_TARGET_PROPERTIES structure [Direct2D], d2d1/D2D1_HWND_RENDER_TARGET_PROPERTIES, direct2d.D2D1_HWND_RENDER_TARGET_PROPERTIES
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_HWND_RENDER_TARGET_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_HWND_RENDER_TARGET_PROPERTIES
 - d2d1/D2D1_HWND_RENDER_TARGET_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_HWND_RENDER_TARGET_PROPERTIES
---

# D2D1_HWND_RENDER_TARGET_PROPERTIES structure


## -description

Contains the HWND, pixel size, and presentation options for an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>.

## -struct-fields

### -field hwnd

Type: <b>HWND</b>

The HWND to which the render target issues the output from its drawing commands.

### -field pixelSize

Type: <b><a href="/windows/win32/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The size of the render target, in pixels.

### -field presentOptions

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options">D2D1_PRESENT_OPTIONS</a></b>

A value that specifies whether the render target retains the frame after it is presented and whether the render target waits for the device to refresh before presenting.

## -remarks

Use this structure when you call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties_constd2d1_hwnd_render_target_properties_id2d1hwndrendertarget)">CreateHwndRenderTarget</a> method to create a new <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>.

For convenience, Direct2D provides the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties">D2D1::HwndRenderTargetProperties</a> function for creating new <b>D2D1_HWND_RENDER_TARGET_PROPERTIES</b> structures.


## Examples

The following example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties_constd2d1_hwnd_render_target_properties_id2d1hwndrendertarget)">CreateHwndRenderTarget</a> method to create an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>. It uses the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties">D2D1::HwndRenderTargetProperties</a> helper function to create a <b>D2D1_HWND_RENDER_TARGET_PROPERTIES</b> structure that contains a handle to a window and the size of the drawing area. Because a <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options">D2D1_PRESENT_OPTIONS</a> value isn't specified, the function uses the default value, <b>D2D1_PRESENT_OPTIONS_NONE</b>.  


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


Code has been omitted from this example.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>

