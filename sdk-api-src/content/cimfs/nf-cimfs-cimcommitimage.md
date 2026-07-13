---
UID: NF:cimfs.CimCommitImage
title: CimCommitImage
description: The CimCommitImage function commits the image represented by the image handle. 
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCommitImage
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
 - CimCommitImage
f1_keywords:
 - CimCommitImage
 - cimfs/CimCommitImage
---

## -description

Commits the image represented by the image handle. 

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**
An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The image handle is invalid
HRESULT_FROM_WIN32(ERROR_SHARING_VIOLATION) – The image handle is still in use by another stream handle or the parent image may be mounted. An image cannot be committed while an open stream handle exists and cannot be overwritten when mounted.

## -remarks
Once the image is committed no additional operations can be performed on the image using the image handle. The handle must still be closed to free its associated resources.

The name of the image committed is determined by the parameters to CimCreateImage. Note, it is an error to commit an image while an open stream handle exists for the image.

## -see-also
