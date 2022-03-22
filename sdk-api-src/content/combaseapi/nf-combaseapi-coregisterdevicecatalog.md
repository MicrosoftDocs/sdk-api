---
UID: NF:combaseapi.CoRegisterDeviceCatalog
title: CoRegisterDeviceCatalog
description: TBD
tech.root: com
ms.date: 03/22/2022
helpviewer_keywords:
 - CoRegisterDeviceCatalog
req.construct-type: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - CoRegisterDeviceCatalog
 - combaseapi/CoRegisterDeviceCatalog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRegisterDeviceCatalog
prerelease: false
---

## -description

Enables a downloaded DLL to register its device catalog interfaces within its running process so that the marshaling code will be able to marshal those interfaces.

## -parameters

### -param deviceInstanceId

Type: \_In\_ **[PCWSTR](/windows/desktop/winprog/windows-data-types)**

A null-terminated string containing the instance identifier of the device to register.

### -param cookie

Type: \_Out\_ **CO_DEVICE_CATALOG_COOKIE\***

Returns an instance of **CO_DEVICE_CATALOG_COOKIE**. You can use this value to revoke the device catalog using **CoRegisterDeviceCatalog**.

## -returns

This function can return the standard return values **E_INVALIDARG**, **E_OUTOFMEMORY**, and **S_OK**.

## -remarks

## -see-also
