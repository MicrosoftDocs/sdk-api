---
UID: NF:cimfs.CimMountImage
title: CimMountImage
description: The CimMountImage function mounts the named image from the location specified by cimPath as a volume with the volume GUID specified by volumeId.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimMountImage
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
 - CimMountImage
f1_keywords:
 - CimMountImage
 - cimfs/CimMountImage
---

## -description

Mounts the named image from the location specified by cimPath as a volume with the volume GUID specified by volumeId.

## -parameters

### -param imageContainingPath

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
The directory that will contain the image created. The caller must have FILE_ADD_FILE and FILE_LIST_DIRECTORY access rights. 

### -param imageName

Type: **[PCWSTR](/windows/desktop/winprog/windows-data-types)**
Provides the name of an existing image within the same imageContainingPath that will be mounted.

### -param mountImageFlags

Type: **[CIM_MOUNT_IMAGE_FLAGS](/windows/win32/api/cimfs/ne-cimfs-cim_mount_image_flags)**

### -param volumeId

Type: **GUID\***
Provides a GUID to be used as the volume GUID of the mounted volume. 

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The caller specified an invalid flag.
HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) – the image path is not found.
HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) – imageName is not found at the path specified.
E_ACCESSEDDENIED – The caller does not have access the image or does not have access to mount a volume.
HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS) – A volume is already mounted with the volume GUID specified.

## -remarks

The mounted volume can be accessed at its volume GUID path as defined by the system. This path is in the form \\?\Volume{GUID}. Mounting the volume allows the image created to be verified using the Windows file system APIs such as CreateFile, FindFirstFile/FindNextFile, GetFileAttributesEx and others.

The image cannot be overwritten while it is mounted.

## -see-also
