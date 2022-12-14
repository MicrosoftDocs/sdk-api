---
UID: NF:http.HttpSetRequestProperty
title: HttpSetRequestProperty function (http.h)
description: Sets a new property or modifies an existing property on the specified request.
helpviewer_keywords: ["HttpServer503VerbosityProperty","HttpServerLengthProperty","HttpServerStateProperty","HttpSetRequestProperty","HttpSetRequestProperty function [HTTP]","http.httpsetrequestproperty","http/HttpSetRequestProperty"]
old-location: http\httpsetrequestproperty.htm
tech.root: http
ms.assetid: 66b14012-ae14-49ff-bf07-c45092f4fddd
ms.date: 03/22/2021
ms.keywords: HttpServer503VerbosityProperty, HttpServerLengthProperty, HttpServerStateProperty, HttpSetRequestProperty, HttpSetRequestProperty function [HTTP], http.httpsetrequestproperty, http/HttpSetRequestProperty
req.header: http.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom:
f1_keywords:
 - HttpSetRequestProperty
 - http/HttpSetRequestProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpSetRequestProperty
---

# HttpSetRequestProperty function


## -description

The **HttpSetRequestProperty** function sets a new property or modifies an existing property on the specified request.

## -parameters

### -param RequestQueueHandle [in]

The handle to the request queue on which the request was received. A request queue is created and its handle returned by a call to the [HttpCreateRequestQueue](/windows/desktop/api/http/nf-http-httpcreaterequestqueue) function.

### -param Id [in]

The opaque ID of the request. This ID is located in the *RequestId* member of the [HTTP\_REQUEST](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) structure returned by [HttpReceiveHttpRequest](/windows/win32/api/http/nf-http-httpreceivehttprequest).

### -param PropertyId [in]

A member of the [HTTP\_REQUEST\_PROPERTY](/windows/desktop/api/http/ne-http-http_request_property) enumeration describing the property type that is set. This must be one of the following:

| **Property** | **Meaning** |
| HttpRequestPropertyStreamError | Sets a stream error on the request. |

### -param Input [in]

A pointer to the buffer that contains the property information.

It must point to one of the following property information types based on the property that is set.

| **Property** | **Configuration Type** |
| HttpRequestPropertyStreamError | [HTTP\_REQUEST\_PROPERTY\_STREAM\_ERROR](/windows/win32/api/http/ns-http-http_request_property_stream_error) structure |

### -param InputPropertySize [in]

The length, in bytes, of the buffer pointed to by the *Input* parameter.

### -param Overlapped [in]

For asynchronous calls, set *pOverlapped* to point to an [OVERLAPPED](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure; for synchronous calls, set it to **NULL**.

A synchronous call blocks until the operation is complete, whereas an asynchronous call immediately returns **ERROR\_IO\_PENDING** and the calling application then uses [GetOverlappedResult](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) or I/O completion ports to determine when the operation is completed. For more information about using [OVERLAPPED](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structures for synchronization, see [Synchronization and Overlapped Input and Output](/windows/desktop/Sync/synchronization-and-overlapped-input-and-output).

## -returns

If the function succeeds, it returns **ERROR\_SUCCESS**.

If the function fails, it returns a [system error code](/windows/desktop/Debug/system-error-codes).

## -see-also

[HttpSetRequestQueueProperty](/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty)
