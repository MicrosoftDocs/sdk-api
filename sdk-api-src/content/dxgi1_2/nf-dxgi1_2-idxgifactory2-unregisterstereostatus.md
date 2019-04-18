---
UID: NF:dxgi1_2.IDXGIFactory2.UnregisterStereoStatus
title: IDXGIFactory2::UnregisterStereoStatus (dxgi1_2.h)
author: windows-sdk-content
description: Unregisters a window or an event to stop it from receiving notification when stereo status changes.
old-location: direct3ddxgi\idxgifactory2_UnregisterStereoStatus.htm
tech.root: direct3ddxgi
ms.assetid: 8E3994C4-DA37-4D17-9F4D-C31E48CDE170
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],UnregisterStereoStatus method, IDXGIFactory2.UnregisterStereoStatus, IDXGIFactory2::UnregisterStereoStatus, UnregisterStereoStatus, UnregisterStereoStatus method [DXGI], UnregisterStereoStatus method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_UnregisterStereoStatus, dxgi1_2/IDXGIFactory2::UnregisterStereoStatus
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
 - IDXGIFactory2.UnregisterStereoStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory2::UnregisterStereoStatus


## -description


Unregisters a window or an event to stop it from receiving notification when stereo status changes.


## -parameters




### -param dwCookie [in]

A key value for the window or event to unregister. The  <a href="https://msdn.microsoft.com/42DA05B8-1490-45B6-B22D-95176EBE7150">IDXGIFactory2::RegisterStereoStatusWindow</a> or  <a href="https://msdn.microsoft.com/912FC8B0-8B66-4203-BF27-8D7186F7CAC0">IDXGIFactory2::RegisterStereoStatusEvent</a> method returns this value. 


## -returns



Returns nothing.




## -remarks



<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>UnregisterStereoStatus</b> has no effect. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

