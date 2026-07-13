---
UID: NC:dxcore_interface.PFN_DXCORE_NOTIFICATION_CALLBACK
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: A callback function (implemented by your application), which is called by a DXCore object for notification events.
tech.root: dxcore
ms.date: 06/10/2019
ms.keywords: PFN_DXCORE_NOTIFICATION_CALLBACK, dxcore_interface.pfn_dxcore_notification_callback
ms.localizationpriority: low
targetos: Windows
ms.service: windows
req.assembly: 
req.construct-type: callback
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
 - LibDef
api_location:
 - dxcore.dll
api_name:
 - PFN_DXCORE_NOTIFICATION_CALLBACK
---

## -description

A callback function (implemented by your application), which is called by a DXCore object for notification events.

## -parameters

### -param notificationType

Type: **[DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype)**

The type of notification representing this invocation. See the table in [DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype) for info about what types are valid with which kinds of objects.

### -param object

Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

The [IDXCoreAdapter](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter) or [IDXCoreAdapterList](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist) object raising the notification.

### -param context [in]

Type: **void\***

A pointer, which may be `nullptr`, to an object containing context info.

## -see-also

[IDXCoreAdapter](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [IDXCoreAdapterList](/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
