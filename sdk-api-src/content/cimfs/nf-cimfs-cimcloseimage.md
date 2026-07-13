---
UID: NF:cimfs.CimCloseImage
title: CimCloseImage
description: The CimCloseImage function frees resources associated with the image handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimCloseImage
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
 - CimCloseImage
f1_keywords:
 - CimCloseImage
 - cimfs/CimCloseImage
---

## -description

Frees resources associated with the image handle.

## -parameters

### -param cimImageHandle

Type: **CIMFS_IMAGE_HANDLE**

An opaque handle that represents a writer for the image. This handle is created using CimCreateImage.

## -remarks

If the image handle is closed before it is committed, any modifications performed on the image using the image handle are discarded. If a stream handle exists for the image, the image resources will not be freed until the stream handle is closed.

## -see-also
