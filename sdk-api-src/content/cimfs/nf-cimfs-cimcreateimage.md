---
UID: NF:cimfs.CimCreateImage
title: CimCreateImage
description: The CimCreateImage function creates a handle representing a new image at the location specified, optionally based on an existing image at that location.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCreateImage
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
 - CimCreateImage
f1_keywords:
 - CimCreateImage
 - cimfs/CimCreateImage
---

## -description

Creates a handle representing a new image at the location specified, optionally based on an existing image at that location.

## -parameters

### -param imageContainingPath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
The directory that will contain the image created. The caller must have FILE_ADD_FILE and FILE_LIST_DIRECTORY access rights. The directory will be opened without sharing write access so image creation within a given image directory must be serialized by the caller.

### -param existingImageName

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
Optionally provides the name of an existing image within the same imageContainingPath that will form the base of the new image. If provided, the existing image can be extended or forked when this image is later committed. This parameter must be NULL and the newImageName parameter must be provided to create an image from scratch.

### -param newImageName

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
Optionally provides the name of a new image to be created within the imageContainingPath. If this parameter is not provided the existingImageName parameter must be provided and the new image will overwrite the existing image. When both existingImageName and newImageName are provided the image will be overwritten if they are the same name or will be forked if they are different names.
When an image is forked the existing image is preserved such that both the existing and the new image can be mounted independently.

### -param cimImageHandle

Receives an opaque handle that represents a writer for the image. This handle may be passed in subsequent routines to modify the image.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_ACCESSDENIED - the caller does not have permissions to the specified image containing path.
E_INVALIDARG –The caller failed to specify existingImageName and newImageName.
HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) – the image containing path does not exist.
HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) - existingImageName is specified and an image by that name is not found in the containing path.
HRESULT_FROM_WIN32(ERROR_FILE_EXISTS) – the newImageName differs from the existingImageName and the newImageName already exists at the path specified.
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – A sharing violation occurred on the image containing path. Only one image handle may be created per image containing path.

## -remarks

## -see-also
