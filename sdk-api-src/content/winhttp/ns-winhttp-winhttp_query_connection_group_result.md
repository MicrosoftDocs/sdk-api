---
UID: NS:winhttp._WINHTTP_QUERY_CONNECTION_GROUP_RESULT
title: WINHTTP_QUERY_CONNECTION_GROUP_RESULT
description: Represents a collection of host connection groups.
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
req.typenames: WINHTTP_QUERY_CONNECTION_GROUP_RESULT, *PWINHTTP_QUERY_CONNECTION_GROUP_RESULT
req.redist: 
f1_keywords:
 - _WINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - winhttp/_WINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - PWINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - winhttp/PWINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - WINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - winhttp/WINHTTP_QUERY_CONNECTION_GROUP_RESULT
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
 - _WINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - PWINHTTP_QUERY_CONNECTION_GROUP_RESULT
 - WINHTTP_QUERY_CONNECTION_GROUP_RESULT
---

## -description

Represents a description of the current state of WinHttp's connections. Retrieved via [WinHttpQueryConnectionGroup](nf-winhttp-winhttpqueryconnectiongroup.md).

## -struct-fields

### -field cHosts

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The number of elements in *pHostConnectionGroups*.

### -field pHostConnectionGroups

Type: **[PWINHTTP_HOST_CONNECTION_GROUP](ns-winhttp-winhttp_host_connection_group.md)**

An array of [WINHTTP_HOST_CONNECTION_GROUP](ns-winhttp-winhttp_host_connection_group.md) objects.

## -remarks

## -see-also

* [WinHttpQueryConnectionGroup](nf-winhttp-winhttpqueryconnectiongroup.md)
* [WINHTTP_HOST_CONNECTION_GROUP](ns-winhttp-winhttp_host_connection_group.md)
