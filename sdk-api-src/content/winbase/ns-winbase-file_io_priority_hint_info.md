---
UID: NS:winbase._FILE_IO_PRIORITY_HINT_INFO
title: FILE_IO_PRIORITY_HINT_INFO (winbase.h)
description: Specifies the priority hint for a file I/O operation.
helpviewer_keywords: ["*PFILE_IO_PRIORITY_HINT_INFO","FILE_IO_PRIORITY_HINT_INFO","FILE_IO_PRIORITY_HINT_INFO structure [Files]","PFILE_IO_PRIORITY_HINT_INFO","PFILE_IO_PRIORITY_HINT_INFO structure pointer [Files]","_FILE_IO_PRIORITY_HINT_INFO","fs.file_io_priority_hint_info","winbase/FILE_IO_PRIORITY_HINT_INFO","winbase/PFILE_IO_PRIORITY_HINT_INFO"]
old-location: fs\file_io_priority_hint_info.htm
tech.root: fs
ms.assetid: a142b8fd-b71c-4449-a8c6-fb23715d1576
ms.date: 12/05/2018
ms.keywords: '*PFILE_IO_PRIORITY_HINT_INFO, FILE_IO_PRIORITY_HINT_INFO, FILE_IO_PRIORITY_HINT_INFO structure [Files], PFILE_IO_PRIORITY_HINT_INFO, PFILE_IO_PRIORITY_HINT_INFO structure pointer [Files], _FILE_IO_PRIORITY_HINT_INFO, fs.file_io_priority_hint_info, winbase/FILE_IO_PRIORITY_HINT_INFO, winbase/PFILE_IO_PRIORITY_HINT_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FILE_IO_PRIORITY_HINT_INFO, *PFILE_IO_PRIORITY_HINT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_IO_PRIORITY_HINT_INFO
 - winbase/_FILE_IO_PRIORITY_HINT_INFO
 - PFILE_IO_PRIORITY_HINT_INFO
 - winbase/PFILE_IO_PRIORITY_HINT_INFO
 - FILE_IO_PRIORITY_HINT_INFO
 - winbase/FILE_IO_PRIORITY_HINT_INFO
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
 - FILE_IO_PRIORITY_HINT_INFO
---

# FILE_IO_PRIORITY_HINT_INFO structure


## -description

Specifies the priority hint for a file I/O operation.

## -struct-fields

### -field PriorityHint

The priority hint. This member is a value from the 
      <a href="/windows/desktop/api/winbase/ne-winbase-priority_hint">PRIORITY_HINT</a> enumeration.

## -remarks

The <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a> function 
    can be used with this structure to associate a priority hint with I/O operations on a file-handle basis. In 
    addition to the idle priority (very low), this function allows normal priority and low priority. Whether these 
    priorities are supported and honored by the underlying drivers depends on their implementation (which is why they 
    are called hints). For more information, see the 
    <a href="https://www.microsoft.com/whdc/driver/priorityio.mspx">I/O Prioritization in Windows Vista</a> 
    white paper on the Windows Hardware Developer Central (WHDC) website.

This structure must be aligned on a <b>LONGLONG</b> (8-byte) boundary.

## -see-also

<a href="/windows/desktop/api/winbase/ne-winbase-priority_hint">PRIORITY_HINT</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>