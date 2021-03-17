---
UID: NS:winioctl._FILE_SET_SPARSE_BUFFER
title: FILE_SET_SPARSE_BUFFER
description: Specifies the sparse state to be set.
helpviewer_keywords: ["*PFILE_SET_SPARSE_BUFFER","FILE_SET_SPARSE_BUFFER","FILE_SET_SPARSE_BUFFER structure [Files]","PFILE_SET_SPARSE_BUFFER","PFILE_SET_SPARSE_BUFFER structure pointer [Files]","fs.file_set_sparse_buffer","winioctl/FILE_SET_SPARSE_BUFFER","winioctl/PFILE_SET_SPARSE_BUFFER"]
old-location: fs\file_set_sparse_buffer.htm
tech.root: fs
ms.assetid: f9c24156-bcd6-423e-b055-18651f4e185e
ms.date: 12/05/2018
ms.keywords: '*PFILE_SET_SPARSE_BUFFER, FILE_SET_SPARSE_BUFFER, FILE_SET_SPARSE_BUFFER structure [Files], PFILE_SET_SPARSE_BUFFER, PFILE_SET_SPARSE_BUFFER structure pointer [Files], fs.file_set_sparse_buffer, winioctl/FILE_SET_SPARSE_BUFFER, winioctl/PFILE_SET_SPARSE_BUFFER'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FILE_SET_SPARSE_BUFFER, *PFILE_SET_SPARSE_BUFFER
req.redist: 
f1_keywords:
 - _FILE_SET_SPARSE_BUFFER
 - winioctl/_FILE_SET_SPARSE_BUFFER
 - PFILE_SET_SPARSE_BUFFER
 - winioctl/PFILE_SET_SPARSE_BUFFER
 - FILE_SET_SPARSE_BUFFER
 - winioctl/FILE_SET_SPARSE_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FILE_SET_SPARSE_BUFFER
---

# FILE_SET_SPARSE_BUFFER structure


## -description

Specifies the sparse state to be set.<b>Windows Server 2003 and Windows XP:  </b>This structure is optional. For more information, see 
      <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a>.

## -struct-fields

### -field SetSparse

If <b>TRUE</b>, makes the file sparse.

If <b>FALSE</b>, makes the file not sparse.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>A value of <b>FALSE</b> for this member is valid only on files that no longer have any 
        sparse regions. For more information, see 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a>.

<b>Windows Server 2003 and Windows XP:  </b>A value of <b>FALSE</b> for this member is not supported. Specifying 
        <b>FALSE</b> will cause the 
        <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a> call to fail.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_sparse">FSCTL_SET_SPARSE</a>