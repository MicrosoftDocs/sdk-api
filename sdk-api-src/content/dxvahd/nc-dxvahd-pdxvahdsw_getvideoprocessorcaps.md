---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorCaps
title: PDXVAHDSW_GetVideoProcessorCaps
author: windows-sdk-content
description: Gets the capabilities of one or more software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.
old-location: mf\pdxvahdsw_getvideoprocessorcaps.htm
tech.root: medfound
ms.assetid: d32fd5e7-b8e8-431f-bc74-b75288ceb01f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorCaps, PDXVAHDSW_GetVideoProcessorCaps callback, PDXVAHDSW_GetVideoProcessorCaps callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorCaps, mf.pdxvahdsw_getvideoprocessorcaps
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PDXVAHDSW_GetVideoProcessorCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessorCaps callback function


## -description


Gets the capabilities of one or more software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processors.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/9319a98d-8f43-4f29-8787-18dec53dff88">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://msdn.microsoft.com/d071dea8-2bab-4768-bdbe-86af08a65dc5">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the video processor will be used.


### -param Count [in]

The number of elements in the <i>pCaps</i> array.


### -param *pCaps [out]

A pointer to an array of <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structures. The function fills the structures with the capabilities of the plug-in video processors.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/d9423b3f-4a4b-49f0-8018-c19a7b663300">IDXVAHD_Device::GetVideoProcessorCaps</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

