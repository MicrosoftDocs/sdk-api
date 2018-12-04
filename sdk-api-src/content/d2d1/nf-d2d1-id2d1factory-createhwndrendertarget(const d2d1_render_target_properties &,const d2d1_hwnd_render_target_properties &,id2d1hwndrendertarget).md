---
UID: NF:d2d1.ID2D1Factory.CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget)
title: ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget)
author: windows-sdk-content
description: Creates an ID2D1HwndRenderTarget, a render target that renders to a window.
old-location: direct2d\ID2D1Factory_CreateHwndRenderTarget_ref_D2D1_RENDER_TARGET_PROPERTIES_ref_D2D1_HWND_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1HwndRenderTarget.htm
tech.root: direct2d
ms.assetid: c1f5f5dd-3ae8-4483-bd7d-f25a69489bab
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CreateHwndRenderTarget, CreateHwndRenderTarget method [Direct2D], CreateHwndRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateHwndRenderTarget method, ID2D1Factory.CreateHwndRenderTarget, ID2D1Factory.CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget), ID2D1Factory::CreateHwndRenderTarget, ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget), d2d1/ID2D1Factory::CreateHwndRenderTarget, direct2d.ID2D1Factory_CreateHwndRenderTarget_ref_D2D1_RENDER_TARGET_PROPERTIES_ref_D2D1_HWND_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1HwndRenderTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateHwndRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateHwndRenderTarget(const D2D1_RENDER_TARGET_PROPERTIES &,const D2D1_HWND_RENDER_TARGET_PROPERTIES &,ID2D1HwndRenderTarget)


## -description


Creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, a render target that renders to a window.


## -parameters




### -param renderTargetProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a></b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering.  For information about supported pixel formats, see  <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>.


### -param hwndRenderTargetProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/4300843a-a24f-4f9e-a396-67172f083638">D2D1_HWND_RENDER_TARGET_PROPERTIES</a></b>

The window handle, initial size (in pixels), and present options.


### -param hwndRenderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a> object created by this method.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error is received. When you receive this error, you need to recreate the render target (and any resources it created).


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>RECT rc;
GetClientRect(m_hwnd, &amp;rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory-&gt;CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &amp;m_pRenderTarget
    );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

