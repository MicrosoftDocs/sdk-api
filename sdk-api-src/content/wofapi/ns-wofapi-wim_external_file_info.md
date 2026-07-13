---
UID: NS:wofapi._WIM_EXTERNAL_FILE_INFO
title: WIM_EXTERNAL_FILE_INFO (wofapi.h)
description: Defines metadata specific to files provided by WOF_PROVIDER_WIM.
helpviewer_keywords: ["*PWIM_EXTERNAL_FILE_INFO","PWIM_EXTERNAL_FILE_INFO","PWIM_EXTERNAL_FILE_INFO structure pointer [Files]","WIM_EXTERNAL_FILE_INFO","WIM_EXTERNAL_FILE_INFO structure [Files]","fs.wim_external_file_info","wofapi/PWIM_EXTERNAL_FILE_INFO","wofapi/WIM_EXTERNAL_FILE_INFO"]
old-location: fs\wim_external_file_info.htm
tech.root: fs
ms.assetid: BB40922B-C9D3-451C-B2D1-1740105C4BAB
ms.date: 12/05/2018
ms.keywords: '*PWIM_EXTERNAL_FILE_INFO, PWIM_EXTERNAL_FILE_INFO, PWIM_EXTERNAL_FILE_INFO structure pointer [Files], WIM_EXTERNAL_FILE_INFO, WIM_EXTERNAL_FILE_INFO structure [Files], fs.wim_external_file_info, wofapi/PWIM_EXTERNAL_FILE_INFO, wofapi/WIM_EXTERNAL_FILE_INFO'
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
req.typenames: WIM_EXTERNAL_FILE_INFO, *PWIM_EXTERNAL_FILE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIM_EXTERNAL_FILE_INFO
 - wofapi/_WIM_EXTERNAL_FILE_INFO
 - PWIM_EXTERNAL_FILE_INFO
 - wofapi/PWIM_EXTERNAL_FILE_INFO
 - WIM_EXTERNAL_FILE_INFO
 - wofapi/WIM_EXTERNAL_FILE_INFO
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
 - WIM_EXTERNAL_FILE_INFO
---

## -description

Defines metadata specific to files provided by WOF_PROVIDER_WIM.

## -struct-fields

### -field DataSourceId

Specifies the data source from which the file’s data is being provided.

### -field Flags

Specifies one or more flags for this data file.  When creating a new backed file, this member should be zero.  When querying the state of an existing file, this member can include WIM_ENTRY_FLAG_NOT_ACTIVE, indicating the data source is removed or the WIM file is not found, or WIM_ENTRY_FLAG_SUSPENDED indicating that the data source is not currently in use but could become in use on demand.

### -field ResourceHash

Specifies the identifier of the file within the WIM file.
