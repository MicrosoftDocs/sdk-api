---
UID: NF:dxgi1_4.IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification
title: IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification (dxgi1_4.h)
description: This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","UnregisterVideoMemoryBudgetChangeNotification method","IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification","IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification","UnregisterVideoMemoryBudgetChangeNotification","UnregisterVideoMemoryBudgetChangeNotification method [DXGI]","UnregisterVideoMemoryBudgetChangeNotification method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_unregistervideomemorybudgetchangenotification","dxgi1_4/IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification"]
old-location: direct3ddxgi\idxgiadapter3_unregistervideomemorybudgetchangenotification.htm
tech.root: direct3ddxgi
ms.assetid: 11695B9E-75B5-44BF-BC09-D377BCEDA341
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],UnregisterVideoMemoryBudgetChangeNotification method, IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification, IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification, UnregisterVideoMemoryBudgetChangeNotification, UnregisterVideoMemoryBudgetChangeNotification method [DXGI], UnregisterVideoMemoryBudgetChangeNotification method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_unregistervideomemorybudgetchangenotification, dxgi1_4/IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification
 - dxgi1_4/IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.UnregisterVideoMemoryBudgetChangeNotification
---

# IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification


## -description

This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

A key value for the window or event to unregister. The  <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a> method returns this value.

## -remarks

An application may switch back to polling for the information regularly.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>