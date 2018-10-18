---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorOutputFormats
title: PDXVAHDSW_GetVideoProcessorOutputFormats
author: windows-sdk-content
description: Gets the output formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessoroutputformats.htm
tech.root: medfound
ms.assetid: d7f767d2-c645-4ade-9b0c-0d5436cf0cfe
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorOutputFormats, PDXVAHDSW_GetVideoProcessorOutputFormats callback, PDXVAHDSW_GetVideoProcessorOutputFormats callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorOutputFormats, mf.pdxvahdsw_getvideoprocessoroutputformats
ms.prod: windows
ms.technology: windows-sdk
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
 - PDXVAHDSW_GetVideoProcessorOutputFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessorOutputFormats callback function


## -description


Gets the output formats that are supported by a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pContentDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/9319a98d-8f43-4f29-8787-18dec53dff88">DXVAHD_CONTENT_DESC</a> structure that describes the video content.


### -param Usage [in]

A member of the <a href="https://msdn.microsoft.com/d071dea8-2bab-4768-bdbe-86af08a65dc5">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used.


### -param Count [in]

The number of formats to retrieve.


### -param *pFormats [out]

A pointer to an array of <b>D3DFORMAT</b> values. The <i>Count</i> parameter specifies the number of elements in the array. The function fills the array with a list of output formats.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/e701014d-c112-42fa-9bf5-88cb31424006">IDXVAHD_Device::GetVideoProcessorOutputFormats</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

