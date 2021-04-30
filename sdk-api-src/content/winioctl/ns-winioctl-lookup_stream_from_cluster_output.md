---
UID: NS:winioctl._LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
title: LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
description: Received as output from the FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code.
helpviewer_keywords: ["*PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT","LOOKUP_STREAM_FROM_CLUSTER_OUTPUT","LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure [Files]","PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT","PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure pointer [Files]","fs.lookup_stream_from_cluster_output","winioctl/LOOKUP_STREAM_FROM_CLUSTER_OUTPUT","winioctl/PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT"]
old-location: fs\lookup_stream_from_cluster_output.htm
tech.root: fs
ms.assetid: 1e9b99eb-93a8-4f0c-98ee-ca9f58466400
ms.date: 12/05/2018
ms.keywords: '*PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT, LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure [Files], PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT, PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure pointer [Files], fs.lookup_stream_from_cluster_output, winioctl/LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, winioctl/PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT'
req.header: winioctl.h
req.include-header: Windows.h
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
req.typenames: LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, *PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT
req.redist: 
f1_keywords:
 - _LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
 - winioctl/_LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
 - PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT
 - winioctl/PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT
 - LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
 - winioctl/LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
---

# LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure


## -description

Received as output from the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control code.

## -struct-fields

### -field Offset

Offset from the beginning of this structure to the first entry returned.  If no entries are returned, this value is zero.

### -field NumberOfMatches

Number of matches to the input criteria.  Note that more matches may be found than entries returned if the buffer provided is not large enough.

### -field BufferSizeRequired

Minimum size of the buffer, in bytes, which would be needed to contain all matching entries to the input criteria.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>