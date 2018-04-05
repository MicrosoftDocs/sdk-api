---
UID: NS:winioctl._FSCTL_QUERY_REGION_INFO_INPUT
title: "_FSCTL_QUERY_REGION_INFO_INPUT"
author: windows-driver-content
description: Contains the storage tier regions from the storage stack for a particular volume.
old-location: fs\fsctl_query_region_info_input.htm
old-project: FileIO
ms.assetid: 2D098A85-F1EA-4538-9BFB-E04092497945
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PFSCTL_QUERY_REGION_INFO_INPUT, FSCTL_QUERY_REGION_INFO_INPUT, FSCTL_QUERY_REGION_INFO_INPUT structure [Files], PFSCTL_QUERY_REGION_INFO_INPUT, PFSCTL_QUERY_REGION_INFO_INPUT structure pointer [Files], _FSCTL_QUERY_REGION_INFO_INPUT, fs.fsctl_query_region_info_input, winioctl/FSCTL_QUERY_REGION_INFO_INPUT, winioctl/PFSCTL_QUERY_REGION_INFO_INPUT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FSCTL_QUERY_REGION_INFO_INPUT, *PFSCTL_QUERY_REGION_INFO_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoctl.h
api_name:
-	FSCTL_QUERY_REGION_INFO_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FSCTL_QUERY_REGION_INFO_INPUT structure


## -description


Contains the storage tier regions from the storage stack for a particular volume.


## -struct-fields




### -field Version

The size of this structure serves as the version.  Set it to <b>sizeof</b>(<b>FSCTL_QUERY_REGION_INFO_INPUT</b>).


### -field Size

The size of this structure in bytes.


### -field Flags

Reserved for future use.


### -field NumberOfTierIds

Number of entries in <b>TierIds</b>, 0 to request IDs for the entire volume.


### -field TierIds

Array of storage tiers (represented by GUID values) for which to return information.

