---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterStereoStatusWindow
title: IDXGIFactory2::RegisterStereoStatusWindow
author: windows-sdk-content
description: Registers an application window to receive notification messages of changes of stereo status.
old-location: direct3ddxgi\idxgifactory2_RegisterStereoStatusWindow.htm
tech.root: direct3ddxgi
ms.assetid: 42DA05B8-1490-45B6-B22D-95176EBE7150
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterStereoStatusWindow method, IDXGIFactory2.RegisterStereoStatusWindow, IDXGIFactory2::RegisterStereoStatusWindow, RegisterStereoStatusWindow, RegisterStereoStatusWindow method [DXGI], RegisterStereoStatusWindow method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_RegisterStereoStatusWindow, dxgi1_2/IDXGIFactory2::RegisterStereoStatusWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIFactory2.RegisterStereoStatusWindow
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
- IDXGIFactory2.RegisterStereoStatusWindow
: 
---

# IDXGIFactory2::RegisterStereoStatusWindow


## -description


Registers an application window to receive notification messages of changes of stereo status.


## -parameters




### -param WindowHandle [in]

The handle of the window to send a notification message to when stereo status change occurs.


### -param wMsg [in]

Identifies the notification message to send. 


### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="https://msdn.microsoft.com/8E3994C4-DA37-4D17-9F4D-C31E48CDE170">IDXGIFactory2::UnregisterStereoStatus</a> method  to unregister the notification message that <i>wMsg</i> specifies.


## -returns



<b>RegisterStereoStatusWindow</b> returns:
        <ul>
<li>S_OK if it successfully registered the window.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>RegisterStereoStatusWindow</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

