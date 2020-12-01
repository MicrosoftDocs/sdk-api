---
UID: NS:wofapi._WOF_FILE_COMPRESSION_INFO_V1
title: WOF_FILE_COMPRESSION_INFO_V1 (wofapi.h)
description: Defines metadata specific to files provided by WOF_PROVIDER_FILE.
helpviewer_keywords: ["*PWOF_FILE_COMPRESSION_INFO_V1","PWOF_FILE_COMPRESSION_INFO_V1","PWOF_FILE_COMPRESSION_INFO_V1 structure pointer [Files]","WOF_FILE_COMPRESSION_INFO","WOF_FILE_COMPRESSION_INFO_V1","WOF_FILE_COMPRESSION_INFO_V1 structure [Files]","fs.wof_file_compression_info_v1","wofapi/PWOF_FILE_COMPRESSION_INFO_V1","wofapi/WOF_FILE_COMPRESSION_INFO_V1"]
old-location: fs\wof_file_compression_info_v1.htm
tech.root: fs
ms.assetid: 84FC5525-43BC-436C-AADC-C58882D48C1F
ms.date: 12/05/2018
ms.keywords: '*PWOF_FILE_COMPRESSION_INFO_V1, PWOF_FILE_COMPRESSION_INFO_V1, PWOF_FILE_COMPRESSION_INFO_V1 structure pointer [Files], WOF_FILE_COMPRESSION_INFO, WOF_FILE_COMPRESSION_INFO_V1, WOF_FILE_COMPRESSION_INFO_V1 structure [Files], fs.wof_file_compression_info_v1, wofapi/PWOF_FILE_COMPRESSION_INFO_V1, wofapi/WOF_FILE_COMPRESSION_INFO_V1'
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WOF_FILE_COMPRESSION_INFO_V1
 - wofapi/_WOF_FILE_COMPRESSION_INFO_V1
 - PWOF_FILE_COMPRESSION_INFO_V1
 - wofapi/PWOF_FILE_COMPRESSION_INFO_V1
 - WOF_FILE_COMPRESSION_INFO_V1
 - wofapi/WOF_FILE_COMPRESSION_INFO_V1
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
 - WOF_FILE_COMPRESSION_INFO_V1
---

# WOF_FILE_COMPRESSION_INFO_V1 structure


## -description

 Defines metadata specific to files provided by WOF_PROVIDER_FILE.

## -struct-fields

### -field Algorithm

Specifies the compression algorithm that is used to compress this file. Currently defined algorithms are: 

<table>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS4K</td>
<td>Indicates that the data for the file should be compressed in 4kb chunks with the XPress algorithm. This algorithm is designed to be computationally lightweight, and provides for rapid access to data.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_LZX</td>
<td>Indicates that the data for the file should be compressed in 32kb chunks with the LZX algorithm. This algorithm is designed to be highly compact, and provides for small footprint for infrequently accessed data.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS8K</td>
<td>Indicates that the data for the file should be compressed in 8kb chunks with the XPress algorithm.</td>
</tr>
<tr>
<td>FILE_PROVIDER_COMPRESSION_XPRESS16K</td>
<td>Indicates that the data for the file should be compressed in 16kb chunks with the XPress algorithm.</td>
</tr>
</table>

### -field Flags

Specifies flags for the operation. Reserved for future use, should be 0.

