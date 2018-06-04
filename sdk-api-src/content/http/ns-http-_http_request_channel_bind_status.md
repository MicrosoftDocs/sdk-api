---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

