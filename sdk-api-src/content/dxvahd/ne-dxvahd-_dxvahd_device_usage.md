---
UID: NE:dxvahd._DXVAHD_DEVICE_USAGE
title: "_DXVAHD_DEVICE_USAGE"
author: windows-driver-content
description: Specifies the intended use for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_device_usage.htm
old-project: medfound
ms.assetid: d071dea8-2bab-4768-bdbe-86af08a65dc5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DXVAHD_DEVICE_USAGE, DXVAHD_DEVICE_USAGE enumeration [Media Foundation], DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY, DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL, _DXVAHD_DEVICE_USAGE, dxvahd/DXVAHD_DEVICE_USAGE, dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY, dxvahd/DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED, dxvahd/DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL, mf.dxvahd_device_usage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: DXVAHD_DEVICE_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_DEVICE_USAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_DEVICE_USAGE enumeration


## -description


Specifies the intended use for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -enum-fields




### -field DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL

Normal video playback. The graphics driver should expose a set of capabilities that are appropriate for real-time video playback.


### -field DXVAHD_DEVICE_USAGE_OPTIMAL_SPEED

Optimal speed.  The graphics driver should expose a minimal set of capabilities that are optimized for performance.

Use this setting if you want better performance and can accept some reduction in video quality. For example, you might use this setting in power-saving mode or to play video thumbnails.


### -field DXVAHD_DEVICE_USAGE_OPTIMAL_QUALITY

Optimal quality. The grahics driver should expose its maximum set of capabilities.

Specify this setting to get the best video quality possible. It is appropriate for tasks such as video editing, when quality is more important than speed. It is not appropriate for real-time playback.


## -remarks



The graphics driver uses one of these enumeration constants as a hint when it creates the DXVA-HD device.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/9a5411f9-2018-4a8a-922d-ab431d615583">DXVAHD_CreateDevice</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

