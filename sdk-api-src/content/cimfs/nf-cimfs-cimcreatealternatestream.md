---
UID: NF:cimfs.CimCreateAlternateStream
title: CimCreateAlternateStream
description: The CimCreateAlternateStream function adds an alternate stream with the specified size at a path relative to the image represented by the image handle.
ms.date: 08/01/2022
ms.keywords: CimCreateAlternateStream
tech.root: cimfs
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
 - CimCreateAlternateStream
f1_keywords:
 - CimCreateAlternateStream
 - cimfs/CimCreateAlternateStream
---

## -description

Adds an alternate stream with the specified size at a path relative to the image represented by the image handle. Provides a handle to the stream which can be used to write data to the stream.

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**
An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.
Only one stream handle can be opened for a given image at a given time. Close the stream handle before opening another stream.

### -param imageRelativePath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
A path relative to the image root where the new stream will be created. The path must refer to an existing file or directory in the image and the stream name must be separated by a ‘:’ character.

### -param streamSize

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**
The size of the stream in bytes. The stream may be written only up to this size. Once the stream is created its size cannot be extended. To extend the stream it must be re-created. The stream will be sparsely allocated in the image such that ranges that are never written contains zeros when read. 

### -param cimStreamHandle

Type: **CIMFS_STREAM_HANDLE\***
An opaque handle that represents a writer for the stream. This handle may be passed in subsequent routines to write the stream.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The image handle is invalid, the relative path is not a valid relative path for an alternate stream. The stream name must have the format imageRelativeFilePath:StreamName.
HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) – parent file or directory for the path specified does not exist in the image.
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – The image handle is in use by another stream handle. Only one stream handle may exist per image handle.

## -remarks

## -see-also
