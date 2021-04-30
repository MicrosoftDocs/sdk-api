---
UID: NS:wmsdkidl._DRM_VAL16
title: DRM_VAL16 (wmsdkidl.h)
description: The DRM_VAL16 structure is used by some DRM-related methods for passing 128-bit device identification values.
helpviewer_keywords: ["DRM_VAL16","DRM_VAL16 structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_val16","wmsdkidl/DRM_VAL16"]
old-location: wmformat\drm_val16.htm
tech.root: wmformat
ms.assetid: 8981042a-f11d-458d-be27-3b1749f9e995
ms.date: 12/05/2018
ms.keywords: DRM_VAL16, DRM_VAL16 structure [windows Media Format], structure [windows Media Format], wmformat.drm_val16, wmsdkidl/DRM_VAL16
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DRM_VAL16
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DRM_VAL16
 - wmsdkidl/_DRM_VAL16
 - DRM_VAL16
 - wmsdkidl/DRM_VAL16
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - DRM_VAL16
---

# DRM_VAL16 structure


## -description

The <b>DRM_VAL16</b> structure is used by some DRM-related methods for passing 128-bit device identification values.

## -struct-fields

### -field val

Array of <b>BYTE</b> values that contains a 128-bit value. Data is stored with the high-order byte in the lowest address (big-endian).

## -remarks

This structure is used to store the device serial number for network devices, such as set-top boxes.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>