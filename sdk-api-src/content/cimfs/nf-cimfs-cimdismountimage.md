---
UID: NF:cimfs.CimDismountImage
title: CimDismountImage
description: The CimDismountImage function dismounts an image mounted with volumeId as the volume GUID.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimDismountImage
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
 - CimDismountImage
f1_keywords:
 - CimDismountImage
 - cimfs/CimDismountImage
---

## -description

Dismounts an image mounted with volumeId as the volume GUID.

## -parameters

### -param volumeId

Type: **GUID\***
Provides the volume GUID of the currently mounted image.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) – The volume GUID specified does not refer to a volume for a mounted CIM image.

## -remarks

## -see-also
