---
UID: NF:winhttp.WinHttpQueryConnectionGroup
title: WinHttpQueryConnectionGroup
description: Retrieves an enumeration of http connections and their **GUID**s.
prerelease: false
tech.root: http
ms.date: 06/16/2021
req.construct-type: function
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - WinHttpQueryConnectionGroup
 - winhttp/WinHttpQueryConnectionGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpQueryConnectionGroup
---

## -description

Retrieves a description of the current state of WinHttp's connections.

## -parameters

### -param hInternet

Type: \_In\_ **[HINTERNET](/windows/win32/winhttp/hinternet-handles-in-winhttp#about-hinternet-handles)**

A request handle or a connect handle.

If a connect handle, then WinHttp assumes that the host uses HTTPS by default. But you can pass **WINHTTP_QUERY_CONNECTION_GROUP_FLAG_INSECURE** (0x0000000000000001ull) in *ullFlags* to indicate that you want non-HTTPS connections.

### -param pGuidConnection

Type: \_In\_ **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)\***

An optional GUID. If provided, then only connections matching the GUID are returned. Otherwise, the function returns all connections to the host (specified in *hInternet* either by a request handle or a connect handle).

### -param ullFlags

Type: \_In\_ **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Flags. Pass **WINHTTP_QUERY_CONNECTION_GROUP_FLAG_INSECURE** to indicate that you want non-HTTPS connections (see *hInternet*).

### -param ppResult

Type: \_Inout\_ **[PWINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md)\***

The address of a pointer to a [WINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md), through which the results are returned.

WinHttp performs an allocation internally, so once you're done with it you must free this pointer by calling [WinHttpFreeQueryConnectionGroupResult](nf-winhttp-winhttpfreequeryconnectiongroupresult.md).

## -returns

## -remarks

## -see-also

* [WINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md)
* [WinHttpFreeQueryConnectionGroupResult](nf-winhttp-winhttpfreequeryconnectiongroupresult.md)
