---
UID: NF:dxgi1_4.IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent
title: IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent (dxgi1_4.h)
description: This method establishes a correlation between a CPU synchronization object and the budget change event.
helpviewer_keywords: ["IDXGIAdapter3 interface [DXGI]","RegisterVideoMemoryBudgetChangeNotificationEvent method","IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent","IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent","RegisterVideoMemoryBudgetChangeNotificationEvent","RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI]","RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI]","IDXGIAdapter3 interface","direct3ddxgi.idxgiadapter3_registervideomemorybudgetchangenotificationevent","dxgi1_4/IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent"]
old-location: direct3ddxgi\idxgiadapter3_registervideomemorybudgetchangenotificationevent.htm
tech.root: direct3ddxgi
ms.assetid: 58ACCDE6-CB33-4BCE-9B15-84F60AC7B905
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],RegisterVideoMemoryBudgetChangeNotificationEvent method, IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent, IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent, RegisterVideoMemoryBudgetChangeNotificationEvent, RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI], RegisterVideoMemoryBudgetChangeNotificationEvent method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_registervideomemorybudgetchangenotificationevent, dxgi1_4/IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent
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
 - IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent
 - dxgi1_4/IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent
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
 - IDXGIAdapter3.RegisterVideoMemoryBudgetChangeNotificationEvent
---

## -description

This method establishes a correlation between a CPU synchronization object and the budget change event.

## -parameters

### -param hEvent [in]

Type: <b>HANDLE</b>

A handle to the event object that the operating system sets when memory budgets change. The <a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> and <a href="/windows/win32/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> functions return this handle.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a key value that you can pass to the <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-unregistervideomemorybudgetchangenotification">IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification</a> method to unregister the notification event that *hEvent* specifies.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

Instead of calling <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">QueryVideoMemoryInfo</a> regularly, applications can use CPU synchronization objects to efficiently wake threads when budget changes occur.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3">IDXGIAdapter3</a>
