---
UID: NS:winioctl._DUPLICATE_EXTENTS_DATA
title: DUPLICATE_EXTENTS_DATA
description: Contains parameters for the FSCTL_DUPLICATE_EXTENTS control code that performs the Block Cloning operation.
helpviewer_keywords: ["*PDUPLICATE_EXTENTS_DATA","DUPLICATE_EXTENTS_DATA","DUPLICATE_EXTENTS_DATA structure [Files]","PDUPLICATE_EXTENTS_DATA","PDUPLICATE_EXTENTS_DATA structure pointer [Files]","fs.duplicate_extents_data","winioctl/DUPLICATE_EXTENTS_DATA","winioctl/PDUPLICATE_EXTENTS_DATA"]
old-location: fs\duplicate_extents_data.htm
tech.root: fs
ms.assetid: 9E2B3AA1-BC28-4458-9882-13F7EFB23756
ms.date: 12/05/2018
ms.keywords: '*PDUPLICATE_EXTENTS_DATA, DUPLICATE_EXTENTS_DATA, DUPLICATE_EXTENTS_DATA structure [Files], PDUPLICATE_EXTENTS_DATA, PDUPLICATE_EXTENTS_DATA structure pointer [Files], fs.duplicate_extents_data, winioctl/DUPLICATE_EXTENTS_DATA, winioctl/PDUPLICATE_EXTENTS_DATA'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: DUPLICATE_EXTENTS_DATA, *PDUPLICATE_EXTENTS_DATA
req.redist: 
f1_keywords:
 - _DUPLICATE_EXTENTS_DATA
 - winioctl/_DUPLICATE_EXTENTS_DATA
 - PDUPLICATE_EXTENTS_DATA
 - winioctl/PDUPLICATE_EXTENTS_DATA
 - DUPLICATE_EXTENTS_DATA
 - winioctl/DUPLICATE_EXTENTS_DATA
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
 - DUPLICATE_EXTENTS_DATA
---

# DUPLICATE_EXTENTS_DATA structure


## -description

Contains parameters for the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file">FSCTL_DUPLICATE_EXTENTS_TO_FILE</a> control code that performs the <a href="/windows/desktop/FileIO/block-cloning">Block Cloning</a> operation.

## -struct-fields

### -field FileHandle

A handle to the source file from which the byte range is to be copied.
To retrieve a file handle, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -field SourceFileOffset

The offset, in bytes, to the beginning of the range to copy from the source file.

### -field TargetFileOffset

The offset, in bytes, to place the copied byte range in the destination file.

### -field ByteCount

The length, in bytes, of the range to copy.

## -see-also

<a href="/windows/desktop/FileIO/block-cloning">Block Cloning</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file">FSCTL_DUPLICATE_EXTENTS_TO_FILE</a>



<a href="/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>