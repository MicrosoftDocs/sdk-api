---
UID: NS:winioctl._LOOKUP_STREAM_FROM_CLUSTER_INPUT
title: LOOKUP_STREAM_FROM_CLUSTER_INPUT
description: Passed as input to the FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code.
helpviewer_keywords: ["*PLOOKUP_STREAM_FROM_CLUSTER_INPUT","LOOKUP_STREAM_FROM_CLUSTER_INPUT","LOOKUP_STREAM_FROM_CLUSTER_INPUT structure [Files]","PLOOKUP_STREAM_FROM_CLUSTER_INPUT","PLOOKUP_STREAM_FROM_CLUSTER_INPUT structure pointer [Files]","fs.lookup_stream_from_cluster_input","winioctl/LOOKUP_STREAM_FROM_CLUSTER_INPUT","winioctl/PLOOKUP_STREAM_FROM_CLUSTER_INPUT"]
old-location: fs\lookup_stream_from_cluster_input.htm
tech.root: fs
ms.assetid: 4b398ae8-a396-4917-bcb8-aa5f5920296f
ms.date: 12/05/2018
ms.keywords: '*PLOOKUP_STREAM_FROM_CLUSTER_INPUT, LOOKUP_STREAM_FROM_CLUSTER_INPUT, LOOKUP_STREAM_FROM_CLUSTER_INPUT structure [Files], PLOOKUP_STREAM_FROM_CLUSTER_INPUT, PLOOKUP_STREAM_FROM_CLUSTER_INPUT structure pointer [Files], fs.lookup_stream_from_cluster_input, winioctl/LOOKUP_STREAM_FROM_CLUSTER_INPUT, winioctl/PLOOKUP_STREAM_FROM_CLUSTER_INPUT'
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
req.typenames: LOOKUP_STREAM_FROM_CLUSTER_INPUT, *PLOOKUP_STREAM_FROM_CLUSTER_INPUT
req.redist: 
f1_keywords:
 - _LOOKUP_STREAM_FROM_CLUSTER_INPUT
 - winioctl/_LOOKUP_STREAM_FROM_CLUSTER_INPUT
 - PLOOKUP_STREAM_FROM_CLUSTER_INPUT
 - winioctl/PLOOKUP_STREAM_FROM_CLUSTER_INPUT
 - LOOKUP_STREAM_FROM_CLUSTER_INPUT
 - winioctl/LOOKUP_STREAM_FROM_CLUSTER_INPUT
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
 - LOOKUP_STREAM_FROM_CLUSTER_INPUT
---

# LOOKUP_STREAM_FROM_CLUSTER_INPUT structure


## -description

Passed as input to the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control 
    code.

## -struct-fields

### -field Flags

Flags for the operation. Currently no flags are defined.

### -field NumberOfClusters

Number of clusters in the following array of clusters. The input buffer must be large enough to contain 
      this number or the operation will fail.

### -field Cluster

An array of one or more clusters to look up.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>