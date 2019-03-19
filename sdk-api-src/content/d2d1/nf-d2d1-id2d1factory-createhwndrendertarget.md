---
UID: NF:d2d1.ID2D1Factory.CreateHwndRenderTarget
title: ID2D1Factory::CreateHwndRenderTarget (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1HwndRenderTarget, a render target that renders to a window.
old-location: direct2d\id2d1factory_createhwndrendertarget.htm
tech.root: Direct2D
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# ID2D1Factory::CreateHwndRenderTarget


## -description


<span>Creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, a render target that renders to a window.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e522cc1-7527-458d-8124-0f0a97089fc6">CreateHwndRenderTarget(D2D1_RENDER_TARGET_PROPERTIES*,D2D1_HWND_RENDER_TARGET_PROPERTIES*,ID2D1HwndRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1f5f5dd-3ae8-4483-bd7d-f25a69489bab">CreateHwndRenderTarget(D2D1_RENDER_TARGET_PROPERTIES&,D2D1_HWND_RENDER_TARGET_PROPERTIES&,ID2D1HwndRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
</table>

## -parameters


## -remarks



When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>. 


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




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

