---
UID: NF:dxgi1_2.IDXGISwapChain1.IsTemporaryMonoSupported
title: IDXGISwapChain1::IsTemporaryMonoSupported
author: windows-sdk-content
description: Determines whether a swap chain supports “temporary mono.”
old-location: direct3ddxgi\idxgiswapchain1_istemporarymonosupported.htm
tech.root: direct3ddxgi
ms.assetid: 0943F04B-15E4-4802-ABD1-3E7F5EF774E5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],IsTemporaryMonoSupported method, IDXGISwapChain1.IsTemporaryMonoSupported, IDXGISwapChain1::IsTemporaryMonoSupported, IsTemporaryMonoSupported, IsTemporaryMonoSupported method [DXGI], IsTemporaryMonoSupported method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_istemporarymonosupported, dxgi1_2/IDXGISwapChain1::IsTemporaryMonoSupported
ms.prod: windows-hardware
ms.technology: windows-devices
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
- apiref
: 
- COM
: 
- dxgi1_2.h
: 
- IDXGISwapChain1.IsTemporaryMonoSupported
: 
---

# IDXGISwapChain1::IsTemporaryMonoSupported


## -description


Determines whether a swap chain supports “temporary mono.”


## -parameters






## -returns



Indicates whether to use the swap chain in temporary mono mode. <b>TRUE</b> indicates that you can use temporary-mono mode; otherwise, <b>FALSE</b>.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>IsTemporaryMonoSupported</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



Temporary mono is a feature where a stereo swap chain can be presented using only the content in the left buffer.  To present using the left buffer as a mono buffer, an application calls the  <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> method with the <a href="https://msdn.microsoft.com/en-us/library/Bb509554(v=VS.85).aspx">DXGI_PRESENT_STEREO_TEMPORARY_MONO</a> 
flag.  All windowed swap chains support temporary mono. However, full-screen swap chains optionally support temporary mono because not all hardware supports temporary mono on full-screen swap chains efficiently.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

