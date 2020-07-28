---
UID: NF:cimfs.CimCommitImage
title: CimCommitImage
ms.date: 9/9/2019
ms.keywords: CimCommitImage
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - 
api_location:
 - cimfs.h
api_name:
 - CimCommitImage
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

