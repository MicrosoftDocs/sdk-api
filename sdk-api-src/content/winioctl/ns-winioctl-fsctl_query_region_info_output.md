---
UID: NS:winioctl._FSCTL_QUERY_REGION_INFO_OUTPUT
title: FSCTL_QUERY_REGION_INFO_OUTPUT
description: Contains information for one or more regions.
helpviewer_keywords: ["*PFSCTL_QUERY_REGION_INFO_OUTPUT","FSCTL_QUERY_REGION_INFO_OUTPUT","FSCTL_QUERY_REGION_INFO_OUTPUT structure [Files]","PFSCTL_QUERY_REGION_INFO_OUTPUT","PFSCTL_QUERY_REGION_INFO_OUTPUT structure pointer [Files]","fs.fsctl_query_region_info_output","winioctl/FSCTL_QUERY_REGION_INFO_OUTPUT","winioctl/PFSCTL_QUERY_REGION_INFO_OUTPUT"]
old-location: fs\fsctl_query_region_info_output.htm
tech.root: fs
ms.assetid: 4DF96C7E-9BC3-4EB8-95AD-3E46DA1C435F
ms.date: 12/05/2018
ms.keywords: '*PFSCTL_QUERY_REGION_INFO_OUTPUT, FSCTL_QUERY_REGION_INFO_OUTPUT, FSCTL_QUERY_REGION_INFO_OUTPUT structure [Files], PFSCTL_QUERY_REGION_INFO_OUTPUT, PFSCTL_QUERY_REGION_INFO_OUTPUT structure pointer [Files], fs.fsctl_query_region_info_output, winioctl/FSCTL_QUERY_REGION_INFO_OUTPUT, winioctl/PFSCTL_QUERY_REGION_INFO_OUTPUT'
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
req.typenames: FSCTL_QUERY_REGION_INFO_OUTPUT, *PFSCTL_QUERY_REGION_INFO_OUTPUT
req.redist: 
f1_keywords:
 - _FSCTL_QUERY_REGION_INFO_OUTPUT
 - winioctl/_FSCTL_QUERY_REGION_INFO_OUTPUT
 - PFSCTL_QUERY_REGION_INFO_OUTPUT
 - winioctl/PFSCTL_QUERY_REGION_INFO_OUTPUT
 - FSCTL_QUERY_REGION_INFO_OUTPUT
 - winioctl/FSCTL_QUERY_REGION_INFO_OUTPUT
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
 - FSCTL_QUERY_REGION_INFO_OUTPUT
---

# FSCTL_QUERY_REGION_INFO_OUTPUT structure


## -description

Contains information for one or more regions.

## -struct-fields

### -field Version

The size of this structure serves as the version.  Set it to <b>sizeof</b>(<b>FSCTL_QUERY_REGION_INFO_OUTPUT</b>).

### -field Size

The size of this structure in bytes.

### -field Flags

Reserved for future use.

### -field Reserved

Reserved for future use.

### -field Alignment

Offset from the beginning of the volume to the first slab of the tiered volume. If the logical disk is made up of multiple tiers and each tier maps to a set of regions then the first tier for the volume contained on the logical disk has a certain offset within the tier that represents the offset of the volume on the logical disk.  The <b>Alignment</b> member contains this value.

### -field TotalNumberOfRegions

Total number of available regions.

### -field NumberOfRegionsReturned

Number of regions that fit in the output.

### -field Regions

<a href="/windows/desktop/api/winioctl/ns-winioctl-file_storage_tier_region">FILE_STORAGE_TIER_REGION</a> struct that contains detailed information for each region.