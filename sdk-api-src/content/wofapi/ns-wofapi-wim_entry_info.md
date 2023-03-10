---
UID: NS:wofapi._WIM_ENTRY_INFO
title: WIM_ENTRY_INFO (wofapi.h)
description: Defines metadata specific to each WIM data source hosted on a volume.
helpviewer_keywords: ["*PWIM_ENTRY_INFO","PWIM_ENTRY_INFO","PWIM_ENTRY_INFO structure pointer [Files]","WIM_ENTRY_INFO","WIM_ENTRY_INFO structure [Files]","fs.wim_entry_info","wofapi/PWIM_ENTRY_INFO","wofapi/WIM_ENTRY_INFO"]
old-location: fs\wim_entry_info.htm
tech.root: fs
ms.assetid: 2631B8AC-22B6-410A-AF3C-6D81FEECFB61
ms.date: 12/05/2018
ms.keywords: '*PWIM_ENTRY_INFO, PWIM_ENTRY_INFO, PWIM_ENTRY_INFO structure pointer [Files], WIM_ENTRY_INFO, WIM_ENTRY_INFO structure [Files], fs.wim_entry_info, wofapi/PWIM_ENTRY_INFO, wofapi/WIM_ENTRY_INFO'
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: WIM_ENTRY_INFO, *PWIM_ENTRY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIM_ENTRY_INFO
 - wofapi/_WIM_ENTRY_INFO
 - PWIM_ENTRY_INFO
 - wofapi/PWIM_ENTRY_INFO
 - WIM_ENTRY_INFO
 - wofapi/WIM_ENTRY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wofapi.h
api_name:
 - WIM_ENTRY_INFO
---

# WIM_ENTRY_INFO structure


## -description

Defines metadata specific to each WIM data source hosted on a volume.

## -struct-fields

### -field WimEntryInfoSize

Specifies the size of the structure.  Should be initialized to sizeof(WIM_ENTRY_INFO).

### -field WimType

Specifies the type of the WIM.  Valid values are WIM_BOOT_OS_WIM and zero, which implies the WIM is not an operating system WIM.

### -field DataSourceId

Specifies a unique identifier for this data source.

### -field WimGuid

Specifies the GUID which is stored in the WIM file’s header.

### -field WimPath

Specifies a full path to the WIM file.

### -field WimIndex

Specifies the index within the WIM which is described by this data source.

### -field Flags

Specifies one or more flags for this data source.  Can include WIM_ENTRY_FLAG_NOT_ACTIVE, indicating a data source which is removed or where the WIM file is not found, or WIM_ENTRY_FLAG_SUSPENDED indicating that the data source is not currently in use but could become in use on demand.  If neither flag is present, the WIM is in active use.

