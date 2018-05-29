---
UID: NF:dxgi1_4.IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent
title: IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent
author: windows-sdk-content
description: This method establishes a correlation between a CPU synchronization object and the budget change event.
old-location: direct3ddxgi\idxgiadapter3_registervideomemorybudgetchangenotificationevent.htm
old-project: direct3ddxgi
ms.assetid: 58ACCDE6-CB33-4BCE-9B15-84F60AC7B905
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],RegisterVideoMemoryBudgetChangeNotificationEvent method, IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent, IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent, RegisterVideoMemoryBudgetChangeNotificationEvent, RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI], RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_registervideomemorybudgetchangenotificationevent, dxgi1_4/IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxgi.dll
api_name:
-	IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent


## -description


This method establishes a correlation between a CPU synchronization object and the budget change event.


## -parameters




### -param hEvent [in]

Type: <b>HANDLE</b>

Specifies a HANDLE for the event.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A key value for the window or event to unregister. The  <a href="https://msdn.microsoft.com/789E6EA1-C590-44F6-A474-851E5CF437A5">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a> method returns this value. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



Instead of calling <a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">QueryVideoMemoryInfo</a> regularly, applications can use CPU synchronization objects to efficiently wake threads when budget changes occur. 




## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

