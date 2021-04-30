---
UID: NF:dxcore_interface.IDXCoreAdapterFactory.IsNotificationTypeSupported
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determines whether a specified notification type is supported by the operating system (OS).
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/17/2019
ms.keywords: IDXCoreAdapterFactory interface,IsNotificationTypeSupported method, IDXCoreAdapterFactory.IsNotificationTypeSupported, IDXCoreAdapterFactory::IsNotificationTypeSupported, IsNotificationTypeSupported, IsNotificationTypeSupported method, IsNotificationTypeSupported method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::IsNotificationTypeSupported, dxcore_interface.idxcoreadapterfactory_isnotificationtypesupported
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
 - IDXCoreAdapterFactory.IsNotificationTypeSupported
---

## -description

Determines whether a specified notification type is supported by the operating system (OS). For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).

## -parameters

### -param notificationType

Type: **[DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype)**

The type of notification that you're querying about support for. See the table in [DXCoreNotificationType](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcorenotificationtype) for info about the notification types.

## -returns

Type: **bool**

Returns `true` if the notification type is supported by the system. Otherwise, returns `false`.

## -remarks

You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS. For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.

## -see-also

[IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [DXCore adapter attribute GUIDs](/windows/win32/dxcore/dxcore-adapter-attribute-guids), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
