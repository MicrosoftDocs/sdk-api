---
UID: NS:winbase._FILE_COMPRESSION_INFO
title: FILE_COMPRESSION_INFO (winbase.h)
description: Receives file compression information.
helpviewer_keywords: ["*PFILE_COMPRESSION_INFO","FILE_COMPRESSION_INFO","FILE_COMPRESSION_INFO structure [Files]","PFILE_COMPRESSION_INFO","PFILE_COMPRESSION_INFO structure pointer [Files]","fileextd/FILE_COMPRESSION_INFO","fileextd/PFILE_COMPRESSION_INFO","fs.file_compression_info","winbase/FILE_COMPRESSION_INFO","winbase/PFILE_COMPRESSION_INFO"]
old-location: fs\file_compression_info.htm
tech.root: fs
ms.assetid: 2f64e7cc-e23c-4e3d-8e17-0e8e38f1ea24
ms.date: 12/05/2018
ms.keywords: '*PFILE_COMPRESSION_INFO, FILE_COMPRESSION_INFO, FILE_COMPRESSION_INFO structure [Files], PFILE_COMPRESSION_INFO, PFILE_COMPRESSION_INFO structure pointer [Files], fileextd/FILE_COMPRESSION_INFO, fileextd/PFILE_COMPRESSION_INFO, fs.file_compression_info, winbase/FILE_COMPRESSION_INFO, winbase/PFILE_COMPRESSION_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: FILE_COMPRESSION_INFO, *PFILE_COMPRESSION_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_COMPRESSION_INFO
 - winbase/_FILE_COMPRESSION_INFO
 - PFILE_COMPRESSION_INFO
 - winbase/PFILE_COMPRESSION_INFO
 - FILE_COMPRESSION_INFO
 - winbase/FILE_COMPRESSION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_COMPRESSION_INFO
---

# FILE_COMPRESSION_INFO structure


## -description

Receives file compression information. Used for any handles. Use only when calling <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

## -struct-fields

### -field CompressedFileSize

The file size of the compressed file.

### -field CompressionFormat

The compression format that is used to compress the file.

### -field CompressionUnitShift

The factor that the compression uses.

### -field ChunkShift

The number of chunks that are shifted by compression.

### -field ClusterShift

The number of clusters that are shifted by compression.

### -field Reserved

Reserved.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>