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

# APO_CONNECTION_PROPERTY structure


## -description


Contains the dynamically changing connection properties.


## -struct-fields




### -field pBuffer

A pointer to the connection buffer. Endpoints use this buffer to read and write
    audio data.


### -field u32ValidFrameCount

The number of valid frames in the connection buffer. An APO  uses the valid frame count to determine the amount of data to read and process in the input buffer. An APO sets the valid frame count
    after writing data into its output connection.


### -field u32BufferFlags

The connection flags for this buffer. This indicates the validity status of the APOs. For more information about these flags, see <a href="https://msdn.microsoft.com/996b56d7-1187-4ed7-b5f5-7d77291113f6">APO_BUFFER_FLAGS</a>.


### -field u32Signature

A tag that identifies a valid <b>APO_CONNECTION_PROPERTY</b> structure. A valid structure is marked as <b>APO_CONNECTION_PROPERTY_SIGNATURE</b>.


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.



