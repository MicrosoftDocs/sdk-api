---
UID: NS:http._HTTP_REQUEST_CHANNEL_BIND_STATUS
title: HTTP_REQUEST_CHANNEL_BIND_STATUS (http.h)
description: HTTP_REQUEST_CHANNEL_BIND_STATUS.
helpviewer_keywords: ["*PHTTP_REQUEST_CHANNEL_BIND_STATUS","HTTP_REQUEST_CHANNEL_BIND_STATUS","HTTP_REQUEST_CHANNEL_BIND_STATUS structure [HTTP]","PHTTP_REQUEST_CHANNEL_BIND_STATUS","PHTTP_REQUEST_CHANNEL_BIND_STATUS structure pointer [HTTP]","http.http_request_channel_bind_status","http/HTTP_REQUEST_CHANNEL_BIND_STATUS","http/PHTTP_REQUEST_CHANNEL_BIND_STATUS"]
old-location: http\http_request_channel_bind_status.htm
tech.root: http
ms.assetid: 70f52486-2632-4e15-998b-4d87a86cb11f
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST_CHANNEL_BIND_STATUS, HTTP_REQUEST_CHANNEL_BIND_STATUS, HTTP_REQUEST_CHANNEL_BIND_STATUS structure [HTTP], PHTTP_REQUEST_CHANNEL_BIND_STATUS, PHTTP_REQUEST_CHANNEL_BIND_STATUS structure pointer [HTTP], http.http_request_channel_bind_status, http/HTTP_REQUEST_CHANNEL_BIND_STATUS, http/PHTTP_REQUEST_CHANNEL_BIND_STATUS'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: HTTP_REQUEST_CHANNEL_BIND_STATUS, *PHTTP_REQUEST_CHANNEL_BIND_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_CHANNEL_BIND_STATUS
 - http/_HTTP_REQUEST_CHANNEL_BIND_STATUS
 - PHTTP_REQUEST_CHANNEL_BIND_STATUS
 - http/PHTTP_REQUEST_CHANNEL_BIND_STATUS
 - HTTP_REQUEST_CHANNEL_BIND_STATUS
 - http/HTTP_REQUEST_CHANNEL_BIND_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_REQUEST_CHANNEL_BIND_STATUS
---

# HTTP_REQUEST_CHANNEL_BIND_STATUS structure


## -description

The <b>HTTP_REQUEST_CHANNEL_BIND_STATUS</b> structure contains secure channel endpoint binding information.

## -struct-fields

### -field ServiceName

A pointer to an <a href="/windows/desktop/api/http/ns-http-http_service_binding_w">HTTP_SERVICE_BINDING_W</a> structure cast to a pointer to an <a href="/windows/desktop/api/http/ns-http-http_service_binding_base">HTTP_SERVICE_BINDING_BASE</a> structure containing the service name  from the client.  This is populated if the request's Channel Binding Token (CBT) is not configured to retrieve service names.

### -field ChannelToken

A pointer to a buffer that contains the secure channel endpoint binding.

### -field ChannelTokenSize

The length of the <b>ChannelToken</b> buffer in bytes.

### -field Flags

Reserved