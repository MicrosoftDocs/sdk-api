---
UID: NF:dxcore_interface.IDXCoreAdapterFactory.RegisterEventNotification
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Registers to receive notifications of specific conditions from a DXCore adapter or adapter list.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,RegisterEventNotification method, IDXCoreAdapterFactory.RegisterEventNotification, IDXCoreAdapterFactory::RegisterEventNotification, RegisterEventNotification, RegisterEventNotification method, RegisterEventNotification method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::RegisterEventNotification, dxcore_interface.idxcoreadapterfactory_registereventnotification
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
 - IDXCoreAdapterFactory.RegisterEventNotification
---

## -description

Registers to receive notifications of specific conditions from a DXCore adapter or adapter list. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).

## -parameters

### -param dxCoreObject [in]

Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

The DXCore object ([IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter) or [IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist)) whose notifications you're subscribing to.

### -param notificationType

Type: **[DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype)**

The type of notification that you're registering for. See the table in [DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype) for info about what types are valid with which kinds of objects.

### -param callbackFunction [in]

Type: **[PFN_DXCORE_NOTIFICATION_CALLBACK](/windows/win32/api/dxcore_interface/nc-dxcore_interface-pfn_dxcore_notification_callback)**

A pointer to a callback function (implemented by your application), which is called by the DXCore object for notification events. For the signature of the function, see [PFN_DXCORE_NOTIFICATION_CALLBACK](/windows/win32/api/dxcore_interface/nc-dxcore_interface-pfn_dxcore_notification_callback).

### -param callbackContext [in]

Type: **void\***

An optional pointer to an object containing context info. This object is passed to your callback function when the notification is raised.

### -param eventCookie [out]

Type: **uint32_t\***

A pointer to a **uint32_t** value. If successful, the function dereferences the pointer and sets the value to a non-zero cookie value representing this registration. Use this cookie value to unregister from the notification by calling [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification). See **Remarks**.

If unsuccessful, the function dereferences the pointer and sets the value to zero, which represents an invalid cookie value.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DXGI_ERROR_INVALID_CALL|*notificationType* is unsupported by the operating system (OS).|
|E_INVALIDARG|`nullptr` was provided for *dxCoreObject*, or if an invalid *notificationType* and *dxCoreObject* combination was provided.|
|E_POINTER|`nullptr` was provided for either *callbackFunction* or *eventCookie*.|

## -remarks

You use **RegisterEventNotification** to register for events raised by [IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist) and [IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter) interfaces. These notification types are supported.

|[DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype)|Supported *dxCoreObject*|Notes|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indicates that the list of adapters meeting your filter criteria has changed. If the adapter list is stale at the time of registration, then your callback is immediately called. This callback occurs at most one time per registration.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indicates that the adapter is no longer valid. If the adapter is invalid at registration time, then your callback is immediately called.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indicates that a memory budgeting event has occurred, and that you should call [IDXCoreAdapter::QueryState](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) (with [DXCoreAdapterState::AdapterMemoryBudget](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate)) to evaluate the current memory budget state. Upon registration, an initial callback will always occur to allow you to query the initial state.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indicates that you should re-evaluate the current crypto session status; for example, by calling [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) to determine the impact of the hardware teardown for a specific [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) interface. Upon registration, an initial callback will always occur to allow you to query the initial state.|

A call to the function that you provide in *callbackFunction* is made asynchronously on a background thread by DXCore when the detected event occurs. No guarantee is made as to the ordering or timing of callbacks&mdash;multiple callbacks may occur in any order, or even simultaneously. It's even possible for your callback to be invoked before **RegisterEventNotification** has completed. In that case, DXCore guarantees that your *eventCookie* is set before your callback is called. Multiple callbacks for a specific registration will be serialized in order.

Callbacks may occur at any time until you call [UnregisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification), and it completes. Callbacks occur on their own threads, and you may make calls into the DXCore API on those threads, including **UnregisterEventNotification**, and releasing of the *dxCoreObject*.

> [!IMPORTANT]
> Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to **RegisterEventNotification**, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification). If you don't do that, then a fatal exception is raised when the situation is detected.

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
