---
UID: NF:combaseapi.CoRevokeDeviceCatalog
title: CoRevokeDeviceCatalog
description: Revokes the registration of a device catalog performed by a previous call to [CoRegisterDeviceCatalog](/windows/win32/api/combaseapi/nf-combaseapi-coregisterdevicecatalog).
tech.root: com
ms.date: 03/25/2022
helpviewer_keywords:
 - CoRevokeDeviceCatalog
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
req.lib: onecore.lib
req.dll: combase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - CoRevokeDeviceCatalog
 - combaseapi/CoRevokeDeviceCatalog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - API-MS-Win-Core-Com-l1-1-3.dll
 - ComBase.dll
api_name:
 - CoRevokeDeviceCatalog
prerelease: false
---

## -description

Revokes the registration of a device catalog performed by a previous call to [CoRegisterDeviceCatalog](/windows/win32/api/combaseapi/nf-combaseapi-coregisterdevicecatalog).

## -parameters

### -param cookie

Type: \_In\_ **CO_DEVICE_CATALOG_COOKIE**

The **CO_DEVICE_CATALOG_COOKIE** that was returned by **CoRegisterDeviceCatalog**.

## -returns

This function can return the standard return values **E_INVALIDARG**, **E_OUTOFMEMORY**, and **S_OK**.

## -remarks

## Examples

For a code example, see [CoRegisterDeviceCatalog](nf-combaseapi-coregisterdevicecatalog.md).

## -see-also

* [CoRegisterDeviceCatalog](nf-combaseapi-coregisterdevicecatalog.md)
