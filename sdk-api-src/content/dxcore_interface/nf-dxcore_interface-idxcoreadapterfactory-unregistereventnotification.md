---
UID: NF:dxcore_interface.IDXCoreAdapterFactory.UnregisterEventNotification
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Unregisters from a notification that you previously registered for.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,UnregisterEventNotification method, IDXCoreAdapterFactory.UnregisterEventNotification, IDXCoreAdapterFactory::UnregisterEventNotification, UnregisterEventNotification, UnregisterEventNotification method, UnregisterEventNotification method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::UnregisterEventNotification, dxcore_interface.idxcoreadapterfactory_unregistereventnotification
ms.localizationpriority: low
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: method
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - COM
api_location:
 - dxcore.dll
api_name:
 - IDXCoreAdapterFactory::UnregisterEventNotification
---

## -description

Unregisters from a notification that you previously registered for. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).

## -parameters

### -param eventCookie

Type: **uint32_t**

The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification)) representing a prior registration that you now wish to unregister for.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|The value of *eventCookie* is not a valid cookie representing a prior registration.|

## -remarks

**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed. DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned. However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.

> [!IMPORTANT]
> Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**. If you don't do that, then a fatal exception is raised when the situation is detected.

Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
