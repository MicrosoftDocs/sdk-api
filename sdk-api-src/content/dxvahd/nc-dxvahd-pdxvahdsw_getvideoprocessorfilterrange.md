---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessorFilterRange
title: PDXVAHDSW_GetVideoProcessorFilterRange
author: windows-sdk-content
description: Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_getvideoprocessorfilterrange.htm
tech.root: medfound
ms.assetid: 3c28ffcf-dad5-4ed1-8b04-12e22fd566a4
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: PDXVAHDSW_GetVideoProcessorFilterRange, PDXVAHDSW_GetVideoProcessorFilterRange callback, PDXVAHDSW_GetVideoProcessorFilterRange callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessorFilterRange, mf.pdxvahdsw_getvideoprocessorfilterrange
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
 - PDXVAHDSW_GetVideoProcessorFilterRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessorFilterRange callback function


## -description


Gets the supported range of image filter values from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param Filter [in]

The type of image filter, specified as a member of the <a href="https://msdn.microsoft.com/e6abac04-c8cb-4130-b48e-fb5d25794d62">DXVAHD_FILTER</a> enumeration.


### -param *pRange [out]

A pointer to a <a href="https://msdn.microsoft.com/cd349ac5-9825-4dc8-8735-5d846abb353b">DXVAHD_FILTER_RANGE_DATA</a> structure. The function fills the structure with the range of values for the specified filter.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/cff587a5-04ed-4f3e-bd05-0cb8d83fffb7">IDXVAHD_Device::GetVideoProcessorFilterRange</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

