---
UID: NF:http.HttpDelegateRequestEx
title: HttpDelegateRequestEx
description: Delegates a request from the source request queue to the target request queue.
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
 - HttpDelegateRequestEx
f1_keywords:
 - HttpDelegateRequestEx
 - http/HttpDelegateRequestEx
dev_langs:
 - c++
---

## -description

Delegates a request from the source request queue to the target request queue.

## -parameters

### -param RequestQueueHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to the source request queue.

### -param DelegateQueueHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to the target request queue.

### -param RequestId

Type: \_In\_ **HTTP_REQUEST_ID**

A unique request ID received with [HttpReceiveHttpRequest](/windows/win32/api/http/nf-http-httpreceivehttprequest).

### -param DelegateUrlGroupId

Type: \_In\_ **HTTP_URL_GROUP_ID**

The url group id of the target url group.

### -param PropertyInfoSetSize

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

The number of entries in the *PropertyInfoSet* array.

### -param PropertyInfoSet

Type: \_In\_ [**PHTTP_DELEGATE_REQUEST_PROPERTY_INFO](/windows/win32/api/http/ns-http-http_delegate_request_property_info)**

An array of properties to be set on request when delegating.

## -returns

A **[ULONG](/windows/win32/winprog/windows-data-types)** containing an [NTSTATUS](/openspecs/windows_protocols/ms-erref/87fba13e-bf06-450e-83b1-9241dc81e781) completion status.

## -remarks

## -see-also
