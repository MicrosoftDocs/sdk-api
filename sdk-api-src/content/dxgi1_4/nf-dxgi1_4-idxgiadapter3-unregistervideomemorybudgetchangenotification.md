---
UID: NF:dxgi1_4.IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification
title: IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification
author: windows-sdk-content
description: This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.
old-location: direct3ddxgi\idxgiadapter3_unregistervideomemorybudgetchangenotification.htm
old-project: direct3ddxgi
ms.assetid: 11695B9E-75B5-44BF-BC09-D377BCEDA341
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],UnregisterVideoMemoryBudgetChangeNotification method, IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification, IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification, UnregisterVideoMemoryBudgetChangeNotification, UnregisterVideoMemoryBudgetChangeNotification method [DXGI], UnregisterVideoMemoryBudgetChangeNotification method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_unregistervideomemorybudgetchangenotification, dxgi1_4/IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification


## -description


This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A key value for the window or event to unregister. The  <a href="https://msdn.microsoft.com/789E6EA1-C590-44F6-A474-851E5CF437A5">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a> method returns this value. 


## -returns



This method does not return a value.




## -remarks



An application may switch back to polling for the information regularly.




## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

