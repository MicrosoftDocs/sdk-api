---
UID: NS:http._HTTP_REQUEST_CHANNEL_BIND_STATUS
title: "_HTTP_REQUEST_CHANNEL_BIND_STATUS"
author: windows-sdk-content
description: HTTP_REQUEST_CHANNEL_BIND_STATUS.
old-location: http\http_request_channel_bind_status.htm
tech.root: Http
ms.assetid: 70f52486-2632-4e15-998b-4d87a86cb11f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_REQUEST_CHANNEL_BIND_STATUS, HTTP_REQUEST_CHANNEL_BIND_STATUS, HTTP_REQUEST_CHANNEL_BIND_STATUS structure [HTTP], PHTTP_REQUEST_CHANNEL_BIND_STATUS, PHTTP_REQUEST_CHANNEL_BIND_STATUS structure pointer [HTTP], _HTTP_REQUEST_CHANNEL_BIND_STATUS, http.http_request_channel_bind_status, http/HTTP_REQUEST_CHANNEL_BIND_STATUS, http/PHTTP_REQUEST_CHANNEL_BIND_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_REQUEST_CHANNEL_BIND_STATUS
product: Windows
targetos: Windows
req.typenames: HTTP_REQUEST_CHANNEL_BIND_STATUS, *PHTTP_REQUEST_CHANNEL_BIND_STATUS
req.redist: 
---

# _HTTP_REQUEST_CHANNEL_BIND_STATUS structure


## -description


The <b>HTTP_REQUEST_CHANNEL_BIND_STATUS</b> structure contains secure channel endpoint binding information.


## -struct-fields




### -field ServiceName

A pointer to an <a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a> structure cast to a pointer to an <a href="https://msdn.microsoft.com/c9d3ed21-8987-4b98-99a1-dc1e776b0dab">HTTP_SERVICE_BINDING_BASE</a> structure containing the service name  from the client.  This is populated if the request's Channel Binding Token (CBT) is not configured to retrieve service names.


### -field ChannelToken

A pointer to a buffer that contains the secure channel endpoint binding.


### -field ChannelTokenSize

The length of the <b>ChannelToken</b> buffer in bytes.


### -field Flags

Reserved

