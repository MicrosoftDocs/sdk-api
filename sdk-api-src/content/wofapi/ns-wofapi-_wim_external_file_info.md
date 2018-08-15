---
UID: NS:wofapi._WIM_EXTERNAL_FILE_INFO
title: "_WIM_EXTERNAL_FILE_INFO"
author: windows-sdk-content
description: Defines metadata specific to files provided by WOF_PROVIDER_WIM.
old-location: fs\wim_external_file_info.htm
old-project: fileio
ms.assetid: BB40922B-C9D3-451C-B2D1-1740105C4BAB
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWIM_EXTERNAL_FILE_INFO, PWIM_EXTERNAL_FILE_INFO, PWIM_EXTERNAL_FILE_INFO structure pointer [Files], WIM_EXTERNAL_FILE_INFO, WIM_EXTERNAL_FILE_INFO structure [Files], _WIM_EXTERNAL_FILE_INFO, fs.wim_external_file_info, wofapi/PWIM_EXTERNAL_FILE_INFO, wofapi/WIM_EXTERNAL_FILE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wofapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WIM_EXTERNAL_FILE_INFO, *PWIM_EXTERNAL_FILE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wofapi.h
api_name:
 - WIM_EXTERNAL_FILE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WIM_EXTERNAL_FILE_INFO structure


## -description


Defines metadata specific to files provided by WOF_PROVIDER_WIM.


## -struct-fields




### -field DataSourceId

Specifies the data source from which the file’s data is being provided.


### -field ResourceHash

 


### -field Flags

Specifies one or more flags for this data file.  When creating a new backed file, this member should be zero.  When querying the state of an existing file, this member can include WIM_ENTRY_FLAG_NOT_ACTIVE, indicating the data source is removed or the WIM file is not found, or WIM_ENTRY_FLAG_SUSPENDED indicating that the data source is not currently in use but could become in use on demand.


#### - ResourceHash[WIM_PROVIDER_HASH_SIZE]

Specifies the identifier of the file within the WIM file.

