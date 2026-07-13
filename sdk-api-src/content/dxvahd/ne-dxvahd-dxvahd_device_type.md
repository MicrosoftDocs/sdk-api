---
UID: NE:dxvahd._DXVAHD_DEVICE_TYPE
title: DXVAHD_DEVICE_TYPE (dxvahd.h)
description: Specifies the type of Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_DEVICE_TYPE","DXVAHD_DEVICE_TYPE enumeration [Media Foundation]","DXVAHD_DEVICE_TYPE_HARDWARE","DXVAHD_DEVICE_TYPE_OTHER","DXVAHD_DEVICE_TYPE_REFERENCE","DXVAHD_DEVICE_TYPE_SOFTWARE","dxvahd/DXVAHD_DEVICE_TYPE","dxvahd/DXVAHD_DEVICE_TYPE_HARDWARE","dxvahd/DXVAHD_DEVICE_TYPE_OTHER","dxvahd/DXVAHD_DEVICE_TYPE_REFERENCE","dxvahd/DXVAHD_DEVICE_TYPE_SOFTWARE","mf.dxvahd_device_type"]
old-location: mf\dxvahd_device_type.htm
tech.root: mf
ms.assetid: c472f2c6-214d-4bb0-ba9d-8dd04ff2a646
ms.date: 12/05/2018
ms.keywords: DXVAHD_DEVICE_TYPE, DXVAHD_DEVICE_TYPE enumeration [Media Foundation], DXVAHD_DEVICE_TYPE_HARDWARE, DXVAHD_DEVICE_TYPE_OTHER, DXVAHD_DEVICE_TYPE_REFERENCE, DXVAHD_DEVICE_TYPE_SOFTWARE, dxvahd/DXVAHD_DEVICE_TYPE, dxvahd/DXVAHD_DEVICE_TYPE_HARDWARE, dxvahd/DXVAHD_DEVICE_TYPE_OTHER, dxvahd/DXVAHD_DEVICE_TYPE_REFERENCE, dxvahd/DXVAHD_DEVICE_TYPE_SOFTWARE, mf.dxvahd_device_type
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_DEVICE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_DEVICE_TYPE
 - dxvahd/_DXVAHD_DEVICE_TYPE
 - DXVAHD_DEVICE_TYPE
 - dxvahd/DXVAHD_DEVICE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_DEVICE_TYPE
---

# DXVAHD_DEVICE_TYPE enumeration


## -description

Specifies the type of Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -enum-fields

### -field DXVAHD_DEVICE_TYPE_HARDWARE:0

Hardware device. Video processing is performed in the GPU by the driver.

### -field DXVAHD_DEVICE_TYPE_SOFTWARE:1

Software device. Video processing is performed in the CPU by a software plug-in.

### -field DXVAHD_DEVICE_TYPE_REFERENCE:2

Reference device. Video processing is performed in the CPU by a software plug-in.

### -field DXVAHD_DEVICE_TYPE_OTHER:3

Other. The device is neither a hardware device nor a software plug-in.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
