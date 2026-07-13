---
UID: NF:cimfs.CimDeletePath
title: CimDeletePath
description: The CimDeletePath function removes the file, stream, directory or hardlink at a path relative to the image represented by the image handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimDeletePath
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
 - CimDeletePath
f1_keywords:
 - CimDeletePath
 - cimfs/CimDeletePath
---

## -description

Removes the file, stream, directory or hardlink at a path relative to the image represented by the image handle.

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**
An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.

### -param imageRelativePath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
A path relative to the image root for the file, directory, alternate stream or hardlink to be deleted. If the path refers to an existing directory, the directory and its entire contents are deleted.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The image handle is invalid, the relative path is not a valid relative path for file.
HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) – The path specified does not exist in the image.
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – The image handle is in use by another stream handle. Only one stream handle may exist per image handle.

## -remarks

Internally CimDeletePath opens and closes a stream handle and only one stream handle can be opened for a given image at a given time. It is an error to call CimDeletePath while a stream handle is opened on the image. Close any open stream handle before deleting a path.

## -see-also
