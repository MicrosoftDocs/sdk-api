---
UID: NS:winioctl._LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
title: "_LOOKUP_STREAM_FROM_CLUSTER_OUTPUT"
author: windows-driver-content
description: Received as output from the FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code.
old-location: fs\lookup_stream_from_cluster_output.htm
old-project: FileIO
ms.assetid: 1e9b99eb-93a8-4f0c-98ee-ca9f58466400
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT, LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure [Files], PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT, PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure pointer [Files], _LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, fs.lookup_stream_from_cluster_output, winioctl/LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, winioctl/PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: LOOKUP_STREAM_FROM_CLUSTER_OUTPUT, *PLOOKUP_STREAM_FROM_CLUSTER_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	LOOKUP_STREAM_FROM_CLUSTER_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _LOOKUP_STREAM_FROM_CLUSTER_OUTPUT structure


## -description


Received as output from the <a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control code.


## -struct-fields




### -field Offset

Offset from the beginning of this structure to the first entry returned.  If no entries are returned, this value is zero.


### -field NumberOfMatches

Number of matches to the input criteria.  Note that more matches may be found than entries returned if the buffer provided is not large enough.


### -field BufferSizeRequired

Minimum size of the buffer, in bytes, which would be needed to contain all matching entries to the input criteria.


## -see-also




<a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

