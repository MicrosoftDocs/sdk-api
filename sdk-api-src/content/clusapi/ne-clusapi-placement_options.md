---
UID: NE:clusapi.PLACEMENT_OPTIONS
title: PLACEMENT_OPTIONS (clusapi.h)
description: Defines options for placing the cluster.
helpviewer_keywords: ["PLACEMENT_OPTIONS","PLACEMENT_OPTIONS enumeration [Failover Cluster]","PLACEMENT_OPTIONS_ALL","PLACEMENT_OPTIONS_CONSIDER_OFFLINE_VMS","PLACEMENT_OPTIONS_DEFAULT_PLACEMENT_OPTIONS","PLACEMENT_OPTIONS_DISABLE_CSV_VM_DEPENDENCY","PLACEMENT_OPTIONS_DONT_USE_CPU","PLACEMENT_OPTIONS_DONT_USE_MEMORY","PLACEMENT_OPTIONS_MIN_VALUE","clusapi/PLACEMENT_OPTIONS","clusapi/PLACEMENT_OPTIONS_ALL","clusapi/PLACEMENT_OPTIONS_CONSIDER_OFFLINE_VMS","clusapi/PLACEMENT_OPTIONS_DEFAULT_PLACEMENT_OPTIONS","clusapi/PLACEMENT_OPTIONS_DISABLE_CSV_VM_DEPENDENCY","clusapi/PLACEMENT_OPTIONS_DONT_USE_CPU","clusapi/PLACEMENT_OPTIONS_DONT_USE_MEMORY","clusapi/PLACEMENT_OPTIONS_MIN_VALUE","mscs.placement_options"]
old-location: mscs\placement_options.htm
tech.root: MsCS
ms.assetid: 21b968c7-3132-4dda-9b27-404026cd525c
ms.date: 12/05/2018
ms.keywords: PLACEMENT_OPTIONS, PLACEMENT_OPTIONS enumeration [Failover Cluster], PLACEMENT_OPTIONS_ALL, PLACEMENT_OPTIONS_CONSIDER_OFFLINE_VMS, PLACEMENT_OPTIONS_DEFAULT_PLACEMENT_OPTIONS, PLACEMENT_OPTIONS_DISABLE_CSV_VM_DEPENDENCY, PLACEMENT_OPTIONS_DONT_USE_CPU, PLACEMENT_OPTIONS_DONT_USE_MEMORY, PLACEMENT_OPTIONS_MIN_VALUE, clusapi/PLACEMENT_OPTIONS, clusapi/PLACEMENT_OPTIONS_ALL, clusapi/PLACEMENT_OPTIONS_CONSIDER_OFFLINE_VMS, clusapi/PLACEMENT_OPTIONS_DEFAULT_PLACEMENT_OPTIONS, clusapi/PLACEMENT_OPTIONS_DISABLE_CSV_VM_DEPENDENCY, clusapi/PLACEMENT_OPTIONS_DONT_USE_CPU, clusapi/PLACEMENT_OPTIONS_DONT_USE_MEMORY, clusapi/PLACEMENT_OPTIONS_MIN_VALUE, mscs.placement_options
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: PLACEMENT_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PLACEMENT_OPTIONS
 - clusapi/PLACEMENT_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - clusapi.h
api_name:
 - PLACEMENT_OPTIONS
---

# PLACEMENT_OPTIONS enumeration


## -description

Defines options for placing the cluster.

This enumeration contains the values for the <a href="/previous-versions/windows/desktop/mscs/clusters-placementoptions">PlacementOptions</a> property.

## -enum-fields

### -field PLACEMENT_OPTIONS_MIN_VALUE:0x00000000

Minimum value

### -field PLACEMENT_OPTIONS_DEFAULT_PLACEMENT_OPTIONS

Default value

### -field PLACEMENT_OPTIONS_DISABLE_CSV_VM_DEPENDENCY:0x00000001

Disable VM cependency

### -field PLACEMENT_OPTIONS_CONSIDER_OFFLINE_VMS:0x00000002

Consider offline VMS

### -field PLACEMENT_OPTIONS_DONT_USE_MEMORY:0x00000004

Don't use memory

### -field PLACEMENT_OPTIONS_DONT_USE_CPU:0x00000008

Don't use CPU

### -field PLACEMENT_OPTIONS_DONT_USE_LOCAL_TEMP_DISK:0x00000010

### -field PLACEMENT_OPTIONS_DONT_RESUME_VMS_WITH_EXISTING_TEMP_DISK:0x00000020

### -field PLACEMENT_OPTIONS_SAVE_VMS_WITH_LOCAL_DISK_ON_DRAIN_OVERWRITE:0x00000040

### -field PLACEMENT_OPTIONS_DONT_RESUME_AVAILABILTY_SET_VMS_WITH_EXISTING_TEMP_DISK:0x00000080

### -field PLACEMENT_OPTIONS_SAVE_AVAILABILTY_SET_VMS_WITH_LOCAL_DISK_ON_DRAIN_OVERWRITE:0x00000100

### -field PLACEMENT_OPTIONS_AVAILABILITY_SET_DOMAIN_AFFINITY:0x00000200

### -field PLACEMENT_OPTIONS_ALL

Maximum value

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
