---
UID: NF:cimfs.CimCreateFile
title: CimCreateFile
description: The CimCreateFile function adds a new file or directory with the specified metadata at a path relative to the image represented by the image handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCreateFile
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: cimfs.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - cimfs.h
api_name:
 - CimCreateFile
f1_keywords:
 - CimCreateFile
 - cimfs/CimCreateFile
---

## -description

Adds a new file or directory with the specified metadata at a path relative to the image represented by the image handle. Returns a stream handle to the primary stream. The stream handle can be used to write data to a file. If the path already exists in the image it is overwritten.
Only one stream handle can be opened for a given image at a given time. Close any existing stream handle before creating another stream.

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**
An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.

### -param imageRelativePath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
A path relative to the image root where the new file or directory will be created. A leading backslash in the path is allowed. If the path refers to an existing file or directory in the image, the existing item will be overwritten.

### -param fileMetadata

Type: **CIMFS_FILE_METADATA\***
Pointer to a structure that contains the metadata for the new file or directory. For files, a size is provided in the metadata. The file may be written up to this size. Once the file is created its size cannot be extended. To extend the file it must be re-created. Ranges in the file that are never written will be read as zero.

### -param cimStreamHandle

Type: **CIMFS_STREAM_HANDLE\***
Receives an opaque handle that represents a writer for the stream. This handle may be passed in subsequent routines to write the stream.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The image handle is invalid, the relative path is not a valid relative path or the fileMetadata fields are malformed.
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – The image handle is in use by another stream handle. Only one stream handle may exist per image handle.

## -remarks

## -see-also
