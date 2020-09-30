---
UID: NF:cimfs.CimDismountImage
title: CimDismountImage
ms.date: 9/9/2019
ms.keywords: CimDismountImage
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

