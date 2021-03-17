---
UID: NS:winioctl._FILE_OBJECTID_BUFFER
title: FILE_OBJECTID_BUFFER
description: Contains an object identifier and user-defined metadata associated with the object identifier.
helpviewer_keywords: ["*PFILE_OBJECTID_BUFFER","FILE_OBJECTID_BUFFER","FILE_OBJECTID_BUFFER structure [Files]","PFILE_OBJECTID_BUFFER","PFILE_OBJECTID_BUFFER structure pointer [Files]","_win32_file_objectid_buffer_str","base.file_objectid_buffer_str","fs.file_objectid_buffer_str","winioctl/FILE_OBJECTID_BUFFER","winioctl/PFILE_OBJECTID_BUFFER"]
old-location: fs\file_objectid_buffer_str.htm
tech.root: fs
ms.assetid: 4d58921c-a3ec-44f3-b077-528db6b1211c
ms.date: 12/05/2018
ms.keywords: '*PFILE_OBJECTID_BUFFER, FILE_OBJECTID_BUFFER, FILE_OBJECTID_BUFFER structure [Files], PFILE_OBJECTID_BUFFER, PFILE_OBJECTID_BUFFER structure pointer [Files], _win32_file_objectid_buffer_str, base.file_objectid_buffer_str, fs.file_objectid_buffer_str, winioctl/FILE_OBJECTID_BUFFER, winioctl/PFILE_OBJECTID_BUFFER'
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
req.typenames: FILE_OBJECTID_BUFFER, *PFILE_OBJECTID_BUFFER
req.redist: 
f1_keywords:
 - _FILE_OBJECTID_BUFFER
 - winioctl/_FILE_OBJECTID_BUFFER
 - PFILE_OBJECTID_BUFFER
 - winioctl/PFILE_OBJECTID_BUFFER
 - FILE_OBJECTID_BUFFER
 - winioctl/FILE_OBJECTID_BUFFER
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
 - FILE_OBJECTID_BUFFER
---

# FILE_OBJECTID_BUFFER structure


## -description

Contains an object identifier and user-defined metadata associated with the object identifier.

## -struct-fields

### -field ObjectId

The identifier that uniquely identifies the file or directory within the volume on which it resides.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.BirthVolumeId

The identifier of the volume on which the object resided when the object identifier was created, or zero if the volume had no object identifier at that time. After copy operations, move operations, or other file operations, this may not be the same as the object identifier of the volume on which the object presently resides.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.BirthObjectId

The object identifier of the object at the time it was created. After copy operations, move operations, or other file operations, this may not be the same as the <b>ObjectId</b> member at present.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.DomainId

Reserved; must be zero.

### -field DUMMYUNIONNAME.ExtendedInfo

User-defined extended data to be set with <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_object_id_extended">FSCTL_SET_OBJECT_ID_EXTENDED</a>. Use this  data  as an alternative  to  the <b>BirthVolumeId</b>, <b>BirthObjectId</b>, and <b>DomainId</b> members.

## -remarks

Object identifiers are used  to track  files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id">FSCTL_CREATE_OR_GET_OBJECT_ID</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_object_id">FSCTL_DELETE_OBJECT_ID</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_object_id">FSCTL_GET_OBJECT_ID</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_object_id">FSCTL_SET_OBJECT_ID</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_object_id_extended">FSCTL_SET_OBJECT_ID_EXTENDED</a>



<a href="/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers">Object Identifiers</a>