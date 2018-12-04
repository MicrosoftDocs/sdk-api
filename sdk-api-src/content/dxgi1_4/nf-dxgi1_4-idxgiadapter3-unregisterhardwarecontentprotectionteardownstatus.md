---
UID: NF:dxgi1_4.IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus
title: IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus
author: windows-sdk-content
description: Unregisters an event to stop it from receiving notification of hardware content protection teardown events.
old-location: direct3ddxgi\idxgiadapter3_unregisterhardwarecontentprotectionteardownstatus.htm
tech.root: direct3ddxgi
ms.assetid: 821F8BFA-FD11-4E3E-BE5A-05A1F1002EE6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],UnregisterHardwareContentProtectionTeardownStatus method, IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus, IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus, UnregisterHardwareContentProtectionTeardownStatus, UnregisterHardwareContentProtectionTeardownStatus method [DXGI], UnregisterHardwareContentProtectionTeardownStatus method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_unregisterhardwarecontentprotectionteardownstatus, dxgi1_4/IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
req.target-type: Windows
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.UnregisterHardwareContentProtectionTeardownStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus


## -description


Unregisters an event to stop it from receiving notification of hardware content protection teardown events.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A key value for the window or event to unregister. The  <a href="https://msdn.microsoft.com/789E6EA1-C590-44F6-A474-851E5CF437A5">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a> method returns this value. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

