---
UID: NE:audioapotypes.APO_BUFFER_FLAGS
title: APO_BUFFER_FLAGS (audioapotypes.h)
description: Defines the buffer validation flags for the APO_CONNECTION_PROPERTY structure associated with each APO connection.
helpviewer_keywords: ["APO_BUFFER_FLAGS","APO_BUFFER_FLAGS enumeration [Remote Desktop Services]","BUFFER_INVALID","BUFFER_SILENT","BUFFER_VALID","audioapotypes/APO_BUFFER_FLAGS","audioapotypes/BUFFER_INVALID","audioapotypes/BUFFER_SILENT","audioapotypes/BUFFER_VALID","termserv.apo_buffer_flags"]
old-location: termserv\apo_buffer_flags.htm
tech.root: coreaudio
ms.assetid: 996b56d7-1187-4ed7-b5f5-7d77291113f6
ms.date: 12/05/2018
ms.keywords: APO_BUFFER_FLAGS, APO_BUFFER_FLAGS enumeration [Remote Desktop Services], BUFFER_INVALID, BUFFER_SILENT, BUFFER_VALID, audioapotypes/APO_BUFFER_FLAGS, audioapotypes/BUFFER_INVALID, audioapotypes/BUFFER_SILENT, audioapotypes/BUFFER_VALID, termserv.apo_buffer_flags
req.header: audioapotypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: APO_BUFFER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APO_BUFFER_FLAGS
 - audioapotypes/APO_BUFFER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioapotypes.h
api_name:
 - APO_BUFFER_FLAGS
---

# APO_BUFFER_FLAGS enumeration


## -description

Defines the buffer validation flags for the <a href="/windows/desktop/api/audioapotypes/ns-audioapotypes-apo_connection_property">APO_CONNECTION_PROPERTY</a> structure associated with each APO connection.

## -enum-fields

### -field BUFFER_INVALID

There is no valid data in  the connection
    buffer. The buffer pointer is valid and the buffer is capable of holding the amount of valid audio data specified in the <a href="/windows/desktop/api/audioapotypes/ns-audioapotypes-apo_connection_property">APO_CONNECTION_PROPERTY</a> structure.
    While processing audio data, the audio engine marks every connection as BUFFER_INVALID before calling <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiooutputendpointrt-getoutputdatapointer">IAudioOutputEndpoint::GetOutputDataPointer</a> or
    <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">IAudioInputEndpointRT::GetInputDataPointer</a>.

### -field BUFFER_VALID

The connection buffer contains valid data. This is the operational state of the connection buffer. The APO sets this flag after it
    starts writing valid data into the buffer.
Capture endpoints should set this flag in the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">GetInputDataPointer</a> method upon successful completion of the call.

### -field BUFFER_SILENT

The connection buffer must be treated as if it contains silence.
    If the endpoint receives an input connection buffer that is identified as BUFFER_SILENT, then the endpoint can assume the data represents silence. When capturing, the endpoint can also set this flag, if necessary for a capture buffer.

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.