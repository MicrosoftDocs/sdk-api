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

# APO_BUFFER_FLAGS enumeration


## -description


Defines the buffer validation flags for the <a href="https://msdn.microsoft.com/dbf7ed62-445e-4f15-bc21-46117e694dc0">APO_CONNECTION_PROPERTY</a> structure associated with each APO connection.


## -enum-fields




### -field BUFFER_INVALID

There is no valid data in  the connection
    buffer. The buffer pointer is valid and the buffer is capable of holding the amount of valid audio data specified in the <a href="https://msdn.microsoft.com/dbf7ed62-445e-4f15-bc21-46117e694dc0">APO_CONNECTION_PROPERTY</a> structure.
    While processing audio data, the audio engine marks every connection as BUFFER_INVALID before calling <a href="https://msdn.microsoft.com/14d69520-3d0c-42ee-8986-9d83b5cff62e">IAudioOutputEndpoint::GetOutputDataPointer</a> or
    <a href="https://msdn.microsoft.com/1da81a49-d421-4643-9be6-b13d45d678f0">IAudioInputEndpointRT::GetInputDataPointer</a>.


### -field BUFFER_VALID

The connection buffer contains valid data. This is the operational state of the connection buffer. The APO sets this flag after it
    starts writing valid data into the buffer.
Capture endpoints should set this flag in the <a href="https://msdn.microsoft.com/1da81a49-d421-4643-9be6-b13d45d678f0">GetInputDataPointer</a> method upon successful completion of the call.


### -field BUFFER_SILENT

The connection buffer must be treated as if it contains silence.
    If the endpoint receives an input connection buffer that is identified as BUFFER_SILENT, then the endpoint can assume the data represents silence. When capturing, the endpoint can also set this flag, if necessary for a capture buffer.


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.



