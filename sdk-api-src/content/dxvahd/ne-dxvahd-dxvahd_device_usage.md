---
UID: NE:dxvahd._DXVAHD_DEVICE_USAGE
title: DXVAHD_DEVICE_USAGE (dxvahd.h)
description: Specifies the intended use for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_DEVICE_USAGE","DXVAHD_DEVICE_USAGE enumeration [Media Foundation]","DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY","DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED","DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL","dxvahd/DXVAHD_DEVICE_USAGE","dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY","dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED","dxvahd/DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL","mf.dxvahd_device_usage"]
old-location: mf\dxvahd_device_usage.htm
tech.root: mf
ms.assetid: d071dea8-2bab-4768-bdbe-86af08a65dc5
ms.date: 12/05/2018
ms.keywords: DXVAHD_DEVICE_USAGE, DXVAHD_DEVICE_USAGE enumeration [Media Foundation], DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY, DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL, dxvahd/DXVAHD_DEVICE_USAGE, dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY, dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED, dxvahd/DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL, mf.dxvahd_device_usage
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
req.typenames: DXVAHD_DEVICE_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_DEVICE_USAGE
 - dxvahd/_DXVAHD_DEVICE_USAGE
 - DXVAHD_DEVICE_USAGE
 - dxvahd/DXVAHD_DEVICE_USAGE
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
 - DXVAHD_DEVICE_USAGE
---

# DXVAHD_DEVICE_USAGE enumeration


## -description

Specifies the intended use for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -enum-fields

### -field DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL:0

Normal video playback. The graphics driver should expose a set of capabilities that are appropriate for real-time video playback.

### -field DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED:1

Optimal speed.  The graphics driver should expose a minimal set of capabilities that are optimized for performance.

Use this setting if you want better performance and can accept some reduction in video quality. For example, you might use this setting in power-saving mode or to play video thumbnails.

### -field DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY:2

Optimal quality. The graphics driver should expose its maximum set of capabilities.

Specify this setting to get the best video quality possible. It is appropriate for tasks such as video editing, when quality is more important than speed. It is not appropriate for real-time playback.

## -remarks

The graphics driver uses one of these enumeration constants as a hint when it creates the DXVA-HD device.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice">DXVAHD_CreateDevice</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
