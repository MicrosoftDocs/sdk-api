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

# IDXGISwapChain::GetContainingOutput


## -description


Get the output (the display monitor) that contains the majority of the client area of the target window.


## -parameters




### -param ppOutput [out]

Type: <b><a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>**</b>

A pointer to the output interface (see <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



If the method succeeds, the output interface will be filled and its reference count incremented. When you are finished with it, be sure to release the interface to avoid a memory leak.

The output is also owned by the adapter on which the swap chain's device was created.

You cannot call <b>GetContainingOutput</b> on a swap chain that you created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.

To determine the output corresponding to such a swap chain, you should call <a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">IDXGIFactory::EnumAdapters</a> and then <a href="https://msdn.microsoft.com/29a826bb-6282-41d1-abf9-642ccb127774">IDXGIAdapter::EnumOutputs</a> to enumerate over all of the available outputs. You should then intersect the bounds of your <a href="https://msdn.microsoft.com/e189b0c0-4a8d-418c-8509-f94130f24226">CoreWindow::Bounds</a> with the desktop coordinates of each output, as reported by <a href="https://msdn.microsoft.com/5215EF2C-9511-4B21-B574-3447FA5896F7">DXGI_OUTPUT_DESC1::DesktopCoordinates</a> or <a href="https://msdn.microsoft.com/7293abb3-81e5-46b2-9987-f60e3ac9eed8">DXGI_OUTPUT_DESC::DesktopCoordinates</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>
 

 

