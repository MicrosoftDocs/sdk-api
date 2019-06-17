---
UID: NE:d3d11.D3D11_VIDEO_USAGE
title: D3D11_VIDEO_USAGE (d3d11.h)
author: windows-sdk-content
description: Specifies the intended use for a video processor.
old-location: mf\d3d11_video_usage.htm
tech.root: medfound
ms.assetid: 11657847-FFDB-42EA-9A29-FDC1F92DF039
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_USAGE, D3D11_VIDEO_USAGE enumeration [Media Foundation], D3D11_VIDEO_USAGE_OPTIMAL_QUALITY, D3D11_VIDEO_USAGE_OPTIMAL_SPEED, D3D11_VIDEO_USAGE_PLAYBACK_NORMAL, d3d11/D3D11_VIDEO_USAGE, d3d11/D3D11_VIDEO_USAGE_OPTIMAL_QUALITY, d3d11/D3D11_VIDEO_USAGE_OPTIMAL_SPEED, d3d11/D3D11_VIDEO_USAGE_PLAYBACK_NORMAL, mf.d3d11_video_usage
ms.topic: enum
f1_keywords: ["d3d11/D3D11_VIDEO_USAGE"]
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_USAGE
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_USAGE
req.redist: 
ms.custom: 19H1
---

# D3D11_VIDEO_USAGE enumeration


## -description


Specifies the intended use for a video processor.


## -enum-fields




### -field D3D11_VIDEO_USAGE_PLAYBACK_NORMAL

Normal video playback. The graphics driver should expose a set of capabilities that are appropriate for real-time video playback.




### -field D3D11_VIDEO_USAGE_OPTIMAL_SPEED

Optimal speed. The graphics driver should expose a minimal set of capabilities that are optimized for performance.



Use this setting if you want better performance and can accept some reduction in video quality. For example, you might use this setting in power-saving mode or to play video thumbnails.




### -field D3D11_VIDEO_USAGE_OPTIMAL_QUALITY

Optimal quality. The grahics driver should expose its maximum set of capabilities.

Specify this setting to get the best video quality possible. It is appropriate for tasks such as video editing, when quality is more important than speed. It is not appropriate for real-time playback.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_content_desc">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
 

 

