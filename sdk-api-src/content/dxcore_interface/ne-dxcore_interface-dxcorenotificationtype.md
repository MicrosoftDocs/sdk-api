---
UID: NE:dxcore_interface.DXCoreNotificationType
title: DXCoreNotificationType
description: Defines constants that specify types of notifications raised by [IDXCoreAdapter](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter) or [IDXCoreAdapterList](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist) objects.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/11/2019
ms.keywords: DXCoreNotificationType enumeration, dxcore_interface.dxcorenotificationtype
ms.localizationpriority: low
ms.topic: reference
targetos: Windows
ms.prod: windows
req.assembly: 
req.construct-type: enumeration
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
 - HeaderDef
api_location:
 - dxcore.dll
api_name:
 - DXCoreNotificationType
---

## -description

Defines constants that specify types of notifications raised by [IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter) or [IDXCoreAdapterList](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist) objects.

You can register and unregister for these notifications by calling [IDXCoreAdapterFactory::RegisterEventNotification](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification) and [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification), respectively.

## -enum-fields

### -field AdapterListStale:0

This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> object when the adapter list becomes stale. The fresh-to-stale transition is one-way, and one-time, so this notification is raised at most one time.

### -field AdapterNoLongerValid:1

This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object when the adapter becomes no longer valid. The valid-to-invalid transition is one-way, and one-time, so this notification is raised at most one time.

### -field AdapterBudgetChange:2

This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object when an adapter budget change occurs. This notification can occur many times. Using this notification is functionally similar to <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent</a>. In response to this event, you should call [IDXCoreAdapter::QueryState](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate) (with [DXCoreAdapterState::AdapterMemoryBudget](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate)) to evaluate the current memory budget state.

### -field AdapterHardwareContentProtectionTeardown:3

This notification is raised by an <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> object to notify of an adapter's hardware content protection teardown. This notification can occur many times. It is functionally similar to <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>. In response to this event, you should re-evaluate the current crypto session status; for example, by calling [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) to determine the impact of the hardware teardown for a specific [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) interface.

## -see-also

[IDXCoreAdapterFactory::RegisterEventNotification](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification), [IDXCoreAdapterFactory::UnregisterEventNotification](/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification), [IDXCoreAdapter](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [IDXCoreAdapterList](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
