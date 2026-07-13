---
UID: NS:winbase._FILE_ID_INFO
title: FILE_ID_INFO (winbase.h)
description: Contains identification information for a file. (FILE_ID_INFO)
helpviewer_keywords: ["*PFILE_ID_INFO","FILE_ID_INFO","FILE_ID_INFO structure [Files]","PFILE_ID_INFO","PFILE_ID_INFO structure pointer [Files]","_FILE_ID_INFO","fs.file_id_info","winbase/FILE_ID_INFO","winbase/PFILE_ID_INFO"]
old-location: fs\file_id_info.htm
tech.root: fs
ms.assetid: e2774e29-1a90-44d6-9001-f73a98be6624
ms.date: 12/05/2018
ms.keywords: '*PFILE_ID_INFO, FILE_ID_INFO, FILE_ID_INFO structure [Files], PFILE_ID_INFO, PFILE_ID_INFO structure pointer [Files], _FILE_ID_INFO, fs.file_id_info, winbase/FILE_ID_INFO, winbase/PFILE_ID_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FILE_ID_INFO, *PFILE_ID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_ID_INFO
 - winbase/_FILE_ID_INFO
 - PFILE_ID_INFO
 - winbase/PFILE_ID_INFO
 - FILE_ID_INFO
 - winbase/FILE_ID_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_ID_INFO
---

# FILE_ID_INFO structure


## -description

Contains identification information for a file. This structure is returned from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function when 
    <b>FileIdInfo</b> is passed in the <i>FileInformationClass</i> 
    parameter.

## -struct-fields

### -field VolumeSerialNumber

The serial number of the volume that contains a file.

### -field FileId

The 128-bit file identifier for the file. The file identifier and the volume serial number uniquely identify 
     a file on a single computer. To determine whether two open handles represent the same file, combine the 
     identifier and the volume serial number for each file and compare them.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-file_id_128">FILE_ID_128</a>



<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>
