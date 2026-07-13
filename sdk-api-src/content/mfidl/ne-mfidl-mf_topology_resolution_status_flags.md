---
UID: NE:mfidl._MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
title: MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS (mfidl.h)
description: Defines status flags for the MF_TOPOLOGY_RESOLUTION_STATUS attribute.
helpviewer_keywords: ["MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE","MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS","MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS","MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration [Media Foundation]","MF_TOPOLOGY_RESOLUTION_SUCCEEDED","e2746378-cf01-4a41-af02-9c3089671120","mf.mf_topology_resolution_status_flags","mfidl/MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE","mfidl/MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS","mfidl/MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS","mfidl/MF_TOPOLOGY_RESOLUTION_SUCCEEDED"]
old-location: mf\mf_topology_resolution_status_flags.htm
tech.root: mf
ms.assetid: e2746378-cf01-4a41-af02-9c3089671120
ms.date: 12/05/2018
ms.keywords: MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE, MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS, MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS, MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration [Media Foundation], MF_TOPOLOGY_RESOLUTION_SUCCEEDED, e2746378-cf01-4a41-af02-9c3089671120, mf.mf_topology_resolution_status_flags, mfidl/MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE, mfidl/MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS, mfidl/MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS, mfidl/MF_TOPOLOGY_RESOLUTION_SUCCEEDED
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
 - mfidl/_MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
 - MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
 - mfidl/MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS
---

# MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration


## -description

Defines status flags for the <a href="/windows/desktop/medfound/mf-topology-resolution-status-attribute">MF_TOPOLOGY_RESOLUTION_STATUS</a> attribute.

## -enum-fields

### -field MF_TOPOLOGY_RESOLUTION_SUCCEEDED:0

The topology was resolved successfully.

### -field MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE:0x1

An optional topology node was rejected because the topology loader could not find a media type for the connection.

### -field MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS:0x2

An optional topology node was rejected because it could not be loaded into a protected process.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
