---
UID: NS:winhttp._WINHTTP_MATCH_CONNECTION_GUID
title: WINHTTP_MATCH_CONNECTION_GUID
description: Represents the GUID of a connection, for purposes of connection-matching.
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
req.typenames: WINHTTP_MATCH_CONNECTION_GUID, *PWINHTTP_MATCH_CONNECTION_GUID
req.redist: 
f1_keywords:
 - _WINHTTP_MATCH_CONNECTION_GUID
 - winhttp/_WINHTTP_MATCH_CONNECTION_GUID
 - PWINHTTP_MATCH_CONNECTION_GUID
 - winhttp/PWINHTTP_MATCH_CONNECTION_GUID
 - WINHTTP_MATCH_CONNECTION_GUID
 - winhttp/WINHTTP_MATCH_CONNECTION_GUID
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
 - _WINHTTP_MATCH_CONNECTION_GUID
 - PWINHTTP_MATCH_CONNECTION_GUID
 - WINHTTP_MATCH_CONNECTION_GUID
---

## -description

Represents the GUID of a connection, for purposes of connection-matching.

See the option flag [**WINHTTP_OPTION_MATCH_CONNECTION_GUID**](/windows/win32/winhttp/option-flags). That option takes as input a **WINHTTP_MATCH_CONNECTION_GUID** value.

## -struct-fields

### -field ConnectionGuid

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

A connection's **GUID**.

When **WINHTTP_OPTION_MATCH_CONNECTION_GUID** is set on a request, WinHttp attempts to serve the request on a connection matching *ConnectionGuid*.

### -field ullFlags

Type: **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Flags.

Due to the nature of connection-matching logic, it's possible for an unmarked connection to be assigned to serve the request (if one is encountered before a matching marked connection is). Set *ullFlags* to **WINHTTP_MATCH_CONNECTION_GUID_FLAG_REQUIRE_MARKED_CONNECTION** if you don't want an unmarked connection to be matched. When using that flag, if no matching marked connection is found, then a new connection is created, and the request is sent on that connection.

## -remarks

## -see-also
