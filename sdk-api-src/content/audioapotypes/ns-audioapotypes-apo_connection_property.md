---
UID: NS:audioapotypes.APO_CONNECTION_PROPERTY
title: APO_CONNECTION_PROPERTY (audioapotypes.h)
description: Contains the dynamically changing connection properties.
helpviewer_keywords: ["APO_CONNECTION_PROPERTY","APO_CONNECTION_PROPERTY structure [Remote Desktop Services]","audioapotypes/APO_CONNECTION_PROPERTY","termserv.apo_connection_property"]
old-location: termserv\apo_connection_property.htm
tech.root: coreaudio
ms.assetid: dbf7ed62-445e-4f15-bc21-46117e694dc0
ms.date: 12/05/2018
ms.keywords: APO_CONNECTION_PROPERTY, APO_CONNECTION_PROPERTY structure [Remote Desktop Services], audioapotypes/APO_CONNECTION_PROPERTY, termserv.apo_connection_property
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
req.typenames: APO_CONNECTION_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APO_CONNECTION_PROPERTY
 - audioapotypes/APO_CONNECTION_PROPERTY
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
 - APO_CONNECTION_PROPERTY
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

The connection flags for this buffer. This indicates the validity status of the APOs. For more information about these flags, see <a href="/windows/desktop/api/audioapotypes/ne-audioapotypes-apo_buffer_flags">APO_BUFFER_FLAGS</a>.

### -field u32Signature

A tag that identifies a valid <b>APO_CONNECTION_PROPERTY</b> structure. A valid structure is marked as <b>APO_CONNECTION_PROPERTY_SIGNATURE</b>. If the value of this field is equal to **APO_CONNECTION_PROPERTY_V2_SIGNATURE**, the structure can be safely typecast to a [APO_CONNECTION_PROPERTY_V2](ns-audioapotypes-apo_connection_property_v2.md).

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.