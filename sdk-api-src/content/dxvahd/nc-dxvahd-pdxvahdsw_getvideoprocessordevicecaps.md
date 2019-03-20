---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorDeviceCaps
title: PDXVAHDSW_GetVideoProcessorDeviceCaps (dxvahd.h)
author: windows-sdk-content
description: Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessordevicecaps.htm
tech.root: medfound
ms.assetid: 09753e3b-7235-4204-ad08-a083a7db4a2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorDeviceCaps, PDXVAHDSW_GetVideoProcessorDeviceCaps callback, PDXVAHDSW_GetVideoProcessorDeviceCaps callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorDeviceCaps, mf.pdxvahdsw_getvideoprocessordevicecaps
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_GetVideoProcessorDeviceCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessorDeviceCaps callback function


## -description


Gets the capabilities of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/9319a98d-8f43-4f29-8787-18dec53dff88">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://msdn.microsoft.com/d071dea8-2bab-4768-bdbe-86af08a65dc5">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used. The value indicates the desired trade-off between speed and video quality.


### -param *pCaps [out]

A pointer to a <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure that receives the device capabilities.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

