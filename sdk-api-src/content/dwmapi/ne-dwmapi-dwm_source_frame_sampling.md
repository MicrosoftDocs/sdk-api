---
UID: NE:dwmapi.DWM_SOURCE_FRAME_SAMPLING
title: DWM_SOURCE_FRAME_SAMPLING
author: windows-sdk-content
description: Flags used by the DwmSetPresentParameters function to specify the frame sampling type.
old-location: dwm\dwm_source_frame_sampling.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\enums\dwm_source_frame_sampling.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWM_SOURCE_FRAME_SAMPLING, DWM_SOURCE_FRAME_SAMPLING enumeration [Desktop Window Manager], DWM_SOURCE_FRAME_SAMPLING_COVERAGE, DWM_SOURCE_FRAME_SAMPLING_LAST, DWM_SOURCE_FRAME_SAMPLING_POINT, _udwm_dwm_source_frame_sampling, _udwm_dwm_source_frame_sampling_cpp, dwm.dwm_source_frame_sampling, dwmapi/DWM_SOURCE_FRAME_SAMPLING, dwmapi/DWM_SOURCE_FRAME_SAMPLING_COVERAGE, dwmapi/DWM_SOURCE_FRAME_SAMPLING_LAST, dwmapi/DWM_SOURCE_FRAME_SAMPLING_POINT, winui._udwm_dwm_source_frame_sampling
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Dwmapi.h
api_name:
 - DWM_SOURCE_FRAME_SAMPLING
product: Windows
targetos: Windows
req.typenames: DWM_SOURCE_FRAME_SAMPLING
req.redist: 
---

# DWM_SOURCE_FRAME_SAMPLING enumeration


## -description


Flags used by the <a href="https://msdn.microsoft.com/en-us/library/Aa969523(v=VS.85).aspx">DwmSetPresentParameters</a> function to specify the frame sampling type.


## -enum-fields




### -field DWM_SOURCE_FRAME_SAMPLING_POINT

Use the first source frame that includes the first refresh of the output frame.


### -field DWM_SOURCE_FRAME_SAMPLING_COVERAGE

Use the source frame that includes the most refreshes of the output frame. In the case of multiple source frames with the same coverage, the last frame is used.


### -field DWM_SOURCE_FRAME_SAMPLING_LAST

The maximum recognized <a href="https://msdn.microsoft.com/en-us/library/Aa969531(v=VS.85).aspx">DWM_SOURCE_FRAME_SAMPLING</a> value, used for validation purposes.

