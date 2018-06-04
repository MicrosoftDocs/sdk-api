---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DXGI_SWAP_CHAIN_DESC structure


## -description


Describes a swap chain.


## -struct-fields




### -field BufferDesc

Type: <b><a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a></b>

A <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a> structure that describes the backbuffer display mode.


### -field SampleDesc

Type: <b><a href="https://msdn.microsoft.com/a8071d3c-dc78-43fe-84f6-421418e16b02">DXGI_SAMPLE_DESC</a></b>

A <a href="https://msdn.microsoft.com/a8071d3c-dc78-43fe-84f6-421418e16b02">DXGI_SAMPLE_DESC</a> structure that describes multi-sampling parameters.


### -field BufferUsage

Type: <b><a href="https://msdn.microsoft.com/b5026566-89b5-458e-b36d-a55e5f8c10c1">DXGI_USAGE</a></b>

A member of the <a href="https://msdn.microsoft.com/b5026566-89b5-458e-b36d-a55e5f8c10c1">DXGI_USAGE</a> enumerated type that describes the surface usage and CPU access options for the back buffer. The back buffer can 
        be used for shader input or render-target output.


### -field BufferCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that describes the number of buffers in the swap chain. When you call  <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">IDXGIFactory::CreateSwapChain</a> to create a full-screen swap chain, you typically include the front buffer in this value. For more information about swap-chain buffers, see Remarks.


### -field OutputWindow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

An <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> handle to the output window. This member must not be <b>NULL</b>.


### -field Windowed

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that specifies whether the output is in windowed mode. <b>TRUE</b> if the output is in windowed mode; otherwise, <b>FALSE</b>. 

We recommend that you create a windowed swap chain and allow the end user to change the swap chain to full screen through <a href="https://msdn.microsoft.com/4762082c-5a61-43a0-b158-a70bbec804d4">IDXGISwapChain::SetFullscreenState</a>; that is, do not set this member to FALSE to force the swap chain to be full screen. However, if you create the swap chain as full screen, also provide the end user with a list of supported display modes through the <b>BufferDesc</b> member because a swap chain that is created with an unsupported display mode might cause the display to go black and prevent the end user from seeing anything. 

For more information about choosing windowed verses full screen, see <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">IDXGIFactory::CreateSwapChain</a>.


### -field SwapEffect

Type: <b><a href="https://msdn.microsoft.com/211d53a9-1332-4e94-abd5-7df7f19094a6">DXGI_SWAP_EFFECT</a></b>

A member of the <a href="https://msdn.microsoft.com/211d53a9-1332-4e94-abd5-7df7f19094a6">DXGI_SWAP_EFFECT</a> enumerated type that describes options for handling the contents of the presentation buffer after 
        presenting a surface.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A member of the <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG</a> enumerated type that describes options for swap-chain behavior.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">GetDesc</a> and <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">CreateSwapChain</a> methods.

In full-screen mode, there is a dedicated front buffer; in windowed mode, the desktop is the front buffer.

If you create a swap chain with one buffer, specifying <b>DXGI_SWAP_EFFECT_SEQUENTIAL</b> does not cause the contents of the single 
      buffer to be swapped with the front buffer.

For performance information about flipping swap-chain buffers in full-screen application, 
      see <a href="https://msdn.microsoft.com/0522ccbf-e754-470a-8199-004fcbaa927d">Full-Screen Application Performance Hints</a>.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">IDXGIFactory::CreateSwapChain</a>



<a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>
 

 

