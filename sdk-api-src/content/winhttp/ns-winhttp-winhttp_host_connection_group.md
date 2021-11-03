---
UID: NS:winhttp._WINHTTP_HOST_CONNECTION_GROUP
title: WINHTTP_HOST_CONNECTION_GROUP
description: Represents a collection of connection groups.
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
req.typenames: WINHTTP_HOST_CONNECTION_GROUP, *PWINHTTP_HOST_CONNECTION_GROUP
req.redist: 
f1_keywords:
 - _WINHTTP_HOST_CONNECTION_GROUP
 - winhttp/_WINHTTP_HOST_CONNECTION_GROUP
 - PWINHTTP_HOST_CONNECTION_GROUP
 - winhttp/PWINHTTP_HOST_CONNECTION_GROUP
 - WINHTTP_HOST_CONNECTION_GROUP
 - winhttp/WINHTTP_HOST_CONNECTION_GROUP
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
 - _WINHTTP_HOST_CONNECTION_GROUP
 - PWINHTTP_HOST_CONNECTION_GROUP
 - WINHTTP_HOST_CONNECTION_GROUP
---

## -description

Represents a collection of connection groups.

## -struct-fields

### -field pwszHost

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A string containing the host name.

### -field cConnectionGroups

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The number of elements in *pConnectionGroups*.

### -field pConnectionGroups

Type: **[PWINHTTP_CONNECTION_GROUP](ns-winhttp-winhttp_connection_group.md)**

An array of [WINHTTP_CONNECTION_GROUP](ns-winhttp-winhttp_connection_group.md) objects.

## -remarks

## -see-also

* [WINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md)
* [WINHTTP_CONNECTION_GROUP](ns-winhttp-winhttp_connection_group.md)
