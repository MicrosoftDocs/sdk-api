---
UID: NF:wofapi.WofFileEnumFiles
title: WofFileEnumFiles function (wofapi.h)
description: Enumerates all of the files which are compressed with a specified compression algorithm on a specified volume.
helpviewer_keywords: ["WofFileEnumFiles","WofFileEnumFiles function [Files]","fs.woffileenumfiles","wofapi/WofFileEnumFiles"]
old-location: fs\woffileenumfiles.htm
tech.root: fs
ms.assetid: 0B3CD8A2-AF4C-4438-B284-03AAA81DE436
ms.date: 12/05/2018
ms.keywords: WofFileEnumFiles, WofFileEnumFiles function [Files], fs.woffileenumfiles, wofapi/WofFileEnumFiles
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WofFileEnumFiles
 - wofapi/WofFileEnumFiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofFileEnumFiles
---

# WofFileEnumFiles function


## -description

Enumerates all of the files which are compressed with a specified compression algorithm on a specified volume.

## -parameters

### -param VolumeName [in]

A full path to the volume containing the files to enumerate.

### -param Algorithm [in]

The compression algorithm to enumerate.  For a list of valid compression algorithms, see <a href="/windows/desktop/api/wofapi/ns-wofapi-wof_file_compression_info_v1">WOF_FILE_COMPRESSION_INFO_V1</a>.  If this value is MAX_ULONG, files compressed with any supported compression algorithm will be returned.

### -param EnumProc [in]

The callback function for each data source. The enumeration will stop if <i>EnumProc</i> returns FALSE.

### -param UserData [in, optional]

User defined data passed to <i>EnumProc</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-enum-external-backing">FSCTL_ENUM_EXTERNAL_BACKING</a>