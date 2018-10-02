---
UID: NF:dxgi1_2.IDXGIFactory2.UnregisterOcclusionStatus
title: IDXGIFactory2::UnregisterOcclusionStatus
author: windows-sdk-content
description: Unregisters a window or an event to stop it from receiving notification when occlusion status changes.
old-location: direct3ddxgi\idxgifactory2_unregisterocclusionstatus.htm
tech.root: direct3ddxgi
ms.assetid: 754A627C-0365-4AF5-A6DF-A8D646254ECF
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGIFactory2 interface [DXGI],UnregisterOcclusionStatus method, IDXGIFactory2.UnregisterOcclusionStatus, IDXGIFactory2::UnregisterOcclusionStatus, UnregisterOcclusionStatus, UnregisterOcclusionStatus method [DXGI], UnregisterOcclusionStatus method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_unregisterocclusionstatus, dxgi1_2/IDXGIFactory2::UnregisterOcclusionStatus
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
 - IDXGIFactory2.UnregisterOcclusionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory2::UnregisterOcclusionStatus


## -description


Unregisters a window or an event to stop it from receiving notification when occlusion status changes.


## -parameters




### -param dwCookie [in]

A key value for the window or event to unregister. The  <a href="https://msdn.microsoft.com/8E8E3C2A-F973-4DC3-A226-DB3FF32F9CC4">IDXGIFactory2::RegisterOcclusionStatusWindow</a> or  <a href="https://msdn.microsoft.com/9DCB6309-C1FF-403F-94E1-ABA769D18170">IDXGIFactory2::RegisterOcclusionStatusEvent</a> method returns this value. 


## -returns



Returns nothing.




## -remarks



<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>UnregisterOcclusionStatus</b> has no effect. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

