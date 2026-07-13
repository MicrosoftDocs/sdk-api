---
UID: NF:cimfs.CimCreateHardLink
title: CimCreateHardLink
description: The CimCreateHardLink function adds a hard link to an existing path relative to the image represented by the image handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCreateHardLink
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
 - CimCreateHardLink
f1_keywords:
 - CimCreateHardLink
 - cimfs/CimCreateHardLink
---

## -description

Adds a hard link to an existing path relative to the image represented by the image handle.

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**
An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.

### -param imageRelativePath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
A path relative to the image root where the new hard link will be created. If the path refers to an existing file, that file will be replaced with a link to the file specified.

### -param existingImageRelativePath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
An existing path relative to the image root that will be hard linked. The path must refer to an existing file in the image. It is an error to pass a path to a directory or alternate stream.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The image handle is invalid, the imageRelativePath or existingImageRelative path is not a valid relative path for file.
HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) – existingImageRelativePath does not exist in the image.
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – The image handle is in use by another stream handle. Only one stream handle may exist per image handle.
E_ACCESSDENIED – The existingImageRelativePath is a directory.

## -remarks

Internally CimCreateHardLink opens and closes a stream handle and only one stream handle can be opened for a given image at a given time. It is an error to call CimCreateHardLink while a stream handle is opened on the image. Close any open stream handle before adding a hard link.

## -see-also
