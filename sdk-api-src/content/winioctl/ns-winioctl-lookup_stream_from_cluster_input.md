---
UID: NS:winioctl._LOOKUP_STREAM_FROM_CLUSTER_INPUT
title: LOOKUP_STREAM_FROM_CLUSTER_INPUT
author: windows-sdk-content
description: Passed as input to the FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code.
old-location: fs\lookup_stream_from_cluster_input.htm
tech.root: fileio
ms.assetid: 4b398ae8-a396-4917-bcb8-aa5f5920296f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLOOKUP_STREAM_FROM_CLUSTER_INPUT, LOOKUP_STREAM_FROM_CLUSTER_INPUT, LOOKUP_STREAM_FROM_CLUSTER_INPUT structure [Files], PLOOKUP_STREAM_FROM_CLUSTER_INPUT, PLOOKUP_STREAM_FROM_CLUSTER_INPUT structure pointer [Files], fs.lookup_stream_from_cluster_input, winioctl/LOOKUP_STREAM_FROM_CLUSTER_INPUT, winioctl/PLOOKUP_STREAM_FROM_CLUSTER_INPUT"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - LOOKUP_STREAM_FROM_CLUSTER_INPUT
product: Windows
targetos: Windows
req.typenames: LOOKUP_STREAM_FROM_CLUSTER_INPUT, *PLOOKUP_STREAM_FROM_CLUSTER_INPUT
req.redist: 
---

# LOOKUP_STREAM_FROM_CLUSTER_INPUT structure


## -description


Passed as input to the 
    <a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control 
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




<a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

