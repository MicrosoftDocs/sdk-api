---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterOcclusionStatusEvent
title: IDXGIFactory2::RegisterOcclusionStatusEvent
author: windows-sdk-content
description: Registers to receive notification of changes in occlusion status by using event signaling.
old-location: direct3ddxgi\idxgifactory2_registerocclusionstatusevent.htm
tech.root: direct3ddxgi
ms.assetid: 9DCB6309-C1FF-403F-94E1-ABA769D18170
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterOcclusionStatusEvent method, IDXGIFactory2.RegisterOcclusionStatusEvent, IDXGIFactory2::RegisterOcclusionStatusEvent, RegisterOcclusionStatusEvent, RegisterOcclusionStatusEvent method [DXGI], RegisterOcclusionStatusEvent method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_registerocclusionstatusevent, dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusEvent
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
 - IDXGIFactory2.RegisterOcclusionStatusEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory2::RegisterOcclusionStatusEvent


## -description


Registers to receive notification of  changes in occlusion status by using event signaling.


## -parameters




### -param hEvent [in]

A handle to the event object that the operating system sets when notification of occlusion status change occurs. The <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function returns this handle.


### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="https://msdn.microsoft.com/754A627C-0365-4AF5-A6DF-A8D646254ECF">IDXGIFactory2::UnregisterOcclusionStatus</a> method  to unregister the notification event that <i>hEvent</i> specifies.


## -returns



<b>RegisterOcclusionStatusEvent</b> returns:
        <ul>
<li>S_OK if the method successfully registered the event.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  if <i>hEvent</i> is not a valid handle or not an event handle. </li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>RegisterOcclusionStatusEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



If you call <b>RegisterOcclusionStatusEvent</b> multiple times with the same event handle, <b>RegisterOcclusionStatusEvent</b> fails with <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>.

If you call <b>RegisterOcclusionStatusEvent</b> multiple times with the different event handles, <b>RegisterOcclusionStatusEvent</b> properly registers the events.




## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

