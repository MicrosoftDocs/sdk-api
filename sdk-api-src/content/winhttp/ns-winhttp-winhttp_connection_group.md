---
UID: NS:winhttp._WINHTTP_CONNECTION_GROUP
title: WINHTTP_CONNECTION_GROUP
description: Represents a connection group.
prerelease: false
tech.root: http
ms.date: 06/16/2021
req.construct-type: structure
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINHTTP_CONNECTION_GROUP, *PWINHTTP_CONNECTION_GROUP
req.redist: 
f1_keywords:
 - _WINHTTP_CONNECTION_GROUP
 - winhttp/_WINHTTP_CONNECTION_GROUP
 - PWINHTTP_CONNECTION_GROUP
 - winhttp/PWINHTTP_CONNECTION_GROUP
 - WINHTTP_CONNECTION_GROUP
 - winhttp/WINHTTP_CONNECTION_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_CONNECTION_GROUP
 - PWINHTTP_CONNECTION_GROUP
 - WINHTTP_CONNECTION_GROUP
---

## -description

Represents a connection group.

## -struct-fields

### -field cConnections

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The number of connections marked with *guidGroup*.

### -field guidGroup

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

A http connection **GUID**.

## -remarks

## -see-also

* [WINHTTP_HOST_CONNECTION_GROUP](ns-winhttp-winhttp_host_connection_group.md)
