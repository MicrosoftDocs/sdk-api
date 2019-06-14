---
UID: NF:dxgi1_2.IDXGISwapChain1.IsTemporaryMonoSupported
title: IDXGISwapChain1::IsTemporaryMonoSupported (dxgi1_2.h)
author: windows-sdk-content
description: Determines whether a swap chain supports “temporary mono.”
old-location: direct3ddxgi\idxgiswapchain1_istemporarymonosupported.htm
tech.root: direct3ddxgi
ms.assetid: 0943F04B-15E4-4802-ABD1-3E7F5EF774E5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],IsTemporaryMonoSupported method, IDXGISwapChain1.IsTemporaryMonoSupported, IDXGISwapChain1::IsTemporaryMonoSupported, IsTemporaryMonoSupported, IsTemporaryMonoSupported method [DXGI], IsTemporaryMonoSupported method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_istemporarymonosupported, dxgi1_2/IDXGISwapChain1::IsTemporaryMonoSupported
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.IsTemporaryMonoSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain1::IsTemporaryMonoSupported


## -description


Determines whether a swap chain supports “temporary mono.”


## -parameters






## -returns



Indicates whether to use the swap chain in temporary mono mode. <b>TRUE</b> indicates that you can use temporary-mono mode; otherwise, <b>FALSE</b>.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>IsTemporaryMonoSupported</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://docs.microsoft.com/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>. 




## -remarks



Temporary mono is a feature where a stereo swap chain can be presented using only the content in the left buffer.  To present using the left buffer as a mono buffer, an application calls the  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> method with the <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_STEREO_TEMPORARY_MONO</a> 
flag.  All windowed swap chains support temporary mono. However, full-screen swap chains optionally support temporary mono because not all hardware supports temporary mono on full-screen swap chains efficiently.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>
 

 

