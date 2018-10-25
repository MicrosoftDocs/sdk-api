---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterStereoStatusEvent
title: IDXGIFactory2::RegisterStereoStatusEvent
author: windows-sdk-content
description: Registers to receive notification of changes in stereo status by using event signaling.
old-location: direct3ddxgi\idxgifactory2_RegisterStereoStatusEvent.htm
tech.root: direct3ddxgi
ms.assetid: 912FC8B0-8B66-4203-BF27-8D7186F7CAC0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterStereoStatusEvent method, IDXGIFactory2.RegisterStereoStatusEvent, IDXGIFactory2::RegisterStereoStatusEvent, RegisterStereoStatusEvent, RegisterStereoStatusEvent method [DXGI], RegisterStereoStatusEvent method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_RegisterStereoStatusEvent, dxgi1_2/IDXGIFactory2::RegisterStereoStatusEvent
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
 - IDXGIFactory2.RegisterStereoStatusEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory2::RegisterStereoStatusEvent


## -description


Registers to receive notification of changes in stereo status by using event signaling.


## -parameters




### -param hEvent [in]

A handle to the event object that the operating system sets when notification of stereo status change occurs. The <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function returns this handle. 


### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="https://msdn.microsoft.com/8E3994C4-DA37-4D17-9F4D-C31E48CDE170">IDXGIFactory2::UnregisterStereoStatus</a> method  to unregister the notification event that <i>hEvent</i> specifies.


## -returns



<b>RegisterStereoStatusEvent</b> returns:
        <ul>
<li>S_OK if it successfully registered the event.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>RegisterStereoStatusEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

