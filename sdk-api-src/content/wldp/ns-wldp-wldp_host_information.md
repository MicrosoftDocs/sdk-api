---
UID: NS:wldp.WLDP_HOST_INFORMATION
tech.root: security
title: WLDP_HOST_INFORMATION
ms.date: 08/23/2022
targetos: Windows
description: A structure identifying the host and source file to be evaluated.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wldp.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.target-type: 
req.typenames: WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wldp.h
api_name:
 - WLDP_HOST_INFORMATION
 - PWLDP_HOST_INFORMATION
f1_keywords:
 - WLDP_HOST_INFORMATION
 - wldp/WLDP_HOST_INFORMATION
 - PWLDP_HOST_INFORMATION
 - wldp/PWLDP_HOST_INFORMATION
dev_langs:
 - c++
helpviewer_keywords:
 - WLDP_HOST_INFORMATION
---

## -description

A structure identifying the host and source file to be evaluated.

## -struct-fields

### -field dwRevision

Must be **WLDP\_HOST\_INFORMATION\_REVISION**.

### -field dwHostId

Enumeration value from [**WLDP\_HOST\_ID**](ne-wldp-wldp_host_id.md) that describes the host ID.

### -field szSource

Full path and script name with the extension. NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.

### -field hSource

In addition to the name, the caller can specify a handle to the file used for validation.

## -remarks

## -see-also

