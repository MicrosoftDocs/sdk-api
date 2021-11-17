---
UID: NF:winhttp.WinHttpFreeQueryConnectionGroupResult
title: WinHttpFreeQueryConnectionGroupResult
description: Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](nf-winhttp-winhttpqueryconnectiongroup.md).
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
 - WinHttpFreeQueryConnectionGroupResult
 - winhttp/WinHttpFreeQueryConnectionGroupResult
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
 - WinHttpFreeQueryConnectionGroupResult
---

## -description

Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](nf-winhttp-winhttpqueryconnectiongroup.md).

## -parameters

### -param pResult

Type: \_Inout\_ **[WINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md)\***

A pointer to the [WINHTTP_QUERY_CONNECTION_GROUP_RESULT](ns-winhttp-winhttp_query_connection_group_result.md) object to free.

## -returns

## -remarks

## -see-also

* [WinHttpQueryConnectionGroup](nf-winhttp-winhttpqueryconnectiongroup.md)
