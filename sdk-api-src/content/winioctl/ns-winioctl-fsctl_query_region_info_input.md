---
UID: NS:winioctl._FSCTL_QUERY_REGION_INFO_INPUT
title: FSCTL_QUERY_REGION_INFO_INPUT
description: Contains the storage tier regions from the storage stack for a particular volume.
helpviewer_keywords: ["*PFSCTL_QUERY_REGION_INFO_INPUT","FSCTL_QUERY_REGION_INFO_INPUT","FSCTL_QUERY_REGION_INFO_INPUT structure [Files]","PFSCTL_QUERY_REGION_INFO_INPUT","PFSCTL_QUERY_REGION_INFO_INPUT structure pointer [Files]","fs.fsctl_query_region_info_input","winioctl/FSCTL_QUERY_REGION_INFO_INPUT","winioctl/PFSCTL_QUERY_REGION_INFO_INPUT"]
old-location: fs\fsctl_query_region_info_input.htm
tech.root: fs
ms.assetid: 2D098A85-F1EA-4538-9BFB-E04092497945
ms.date: 12/05/2018
ms.keywords: '*PFSCTL_QUERY_REGION_INFO_INPUT, FSCTL_QUERY_REGION_INFO_INPUT, FSCTL_QUERY_REGION_INFO_INPUT structure [Files], PFSCTL_QUERY_REGION_INFO_INPUT, PFSCTL_QUERY_REGION_INFO_INPUT structure pointer [Files], fs.fsctl_query_region_info_input, winioctl/FSCTL_QUERY_REGION_INFO_INPUT, winioctl/PFSCTL_QUERY_REGION_INFO_INPUT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FSCTL_QUERY_REGION_INFO_INPUT, *PFSCTL_QUERY_REGION_INFO_INPUT
req.redist: 
f1_keywords:
 - _FSCTL_QUERY_REGION_INFO_INPUT
 - winioctl/_FSCTL_QUERY_REGION_INFO_INPUT
 - PFSCTL_QUERY_REGION_INFO_INPUT
 - winioctl/PFSCTL_QUERY_REGION_INFO_INPUT
 - FSCTL_QUERY_REGION_INFO_INPUT
 - winioctl/FSCTL_QUERY_REGION_INFO_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - FSCTL_QUERY_REGION_INFO_INPUT
---

# FSCTL_QUERY_REGION_INFO_INPUT structure


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

