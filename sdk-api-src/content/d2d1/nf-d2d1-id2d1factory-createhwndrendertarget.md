---
UID: NF:d2d1.ID2D1Factory.CreateHwndRenderTarget
title: ID2D1Factory::CreateHwndRenderTarget (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1HwndRenderTarget, a render target that renders to a window.
old-location: direct2d\id2d1factory_createhwndrendertarget.htm
tech.root: Direct2D
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateHwndRenderTarget, CreateHwndRenderTarget methods [Direct2D], ID2D1Factory.CreateHwndRenderTarget, ID2D1Factory::CreateHwndRenderTarget, d2d1/CreateHwndRenderTarget, direct2d.id2d1factory_createhwndrendertarget
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory::CreateHwndRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory::CreateHwndRenderTarget


## -description


<span>Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, a render target that renders to a window.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)">CreateHwndRenderTarget(D2D1_RENDER_TARGET_PROPERTIES*,D2D1_HWND_RENDER_TARGET_PROPERTIES*,ID2D1HwndRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)">CreateHwndRenderTarget(D2D1_RENDER_TARGET_PROPERTIES&,D2D1_HWND_RENDER_TARGET_PROPERTIES&,ID2D1HwndRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
</table>

## -parameters


## -remarks



When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).


#### Examples

The following example creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>. 


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




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
 

 

