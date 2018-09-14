---
UID: NF:dxgi1_3.IDXGISwapChain2.SetSourceSize
title: IDXGISwapChain2::SetSourceSize
author: windows-sdk-content
description: Sets the source region to be used for the swap chain.
old-location: direct3ddxgi\idxgioutpu2_setsourcesize.htm
tech.root: direct3ddxgi
ms.assetid: BD424F5A-9735-4E90-9FAD-A0B827D7AD80
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDXGISwapChain2 interface [DXGI],SetSourceSize method, IDXGISwapChain2.SetSourceSize, IDXGISwapChain2::SetSourceSize, SetSourceSize, SetSourceSize method [DXGI], SetSourceSize method [DXGI],IDXGISwapChain2 interface, direct3ddxgi.idxgioutpu2_setsourcesize, dxgi1_3/IDXGISwapChain2::SetSourceSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2.SetSourceSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain2::SetSourceSize


## -description


Sets the source region to be used for the swap chain.

Use <b>SetSourceSize</b> to specify the portion of the swap chain from which the operating system presents. This allows an effective resize without calling the more-expensive <a href="https://msdn.microsoft.com/c70aaad0-e742-4ff1-9d25-80d171f3f9de">IDXGISwapChain::ResizeBuffers</a> method. Prior to Windows 8.1, calling <b>IDXGISwapChain::ResizeBuffers</b> was the only way to resize the swap chain. The source rectangle is always defined by the region [0, 0, Width, Height].


## -parameters




### -param Width

Source width to use for the swap chain. This value must be greater than zero, and must be less than or equal to the overall width of the swap chain.


### -param Height

Source height to use for the swap chain. This value must be greater than zero, and must be less than or equal to the overall height of the swap chain.


## -returns



This method can return:

<ul>
<li>E_INVALIDARG if one or more parameters exceed the size of the back buffer.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/C7E9BC13-74E5-4981-8F87-390F95B71AE0">GetSourceSize</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>
 

 

