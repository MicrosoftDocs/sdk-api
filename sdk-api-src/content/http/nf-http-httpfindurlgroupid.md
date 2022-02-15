---
UID: NF:http.HttpFindUrlGroupId
title: HttpFindUrlGroupId
description: Retrieves a URL group ID for a URL and a request queue.
ms.date: 11/20/2020
tech.root: http
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Httpapi.dll
req.header: http.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Httpapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpFindUrlGroupId
f1_keywords:
 - HttpFindUrlGroupId
 - http/HttpFindUrlGroupId
dev_langs:
 - c++
---

## -description

Retrieves a URL group ID for a URL and a request queue.

## -parameters

### -param FullyQualifiedUrl

Type: \_In\_ **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The URL whose URL group to query.

### -param RequestQueueHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

The request queue associated with the URL group.

### -param UrlGroupId

Type: \_Out\_ **PHTTP_URL_GROUP_ID**

The matching URL group ID.

## -returns

A **[ULONG](/windows/win32/winprog/windows-data-types)** containing an [NTSTATUS](/openspecs/windows_protocols/ms-erref/87fba13e-bf06-450e-83b1-9241dc81e781) completion status.

## -remarks

## -see-also
