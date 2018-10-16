---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
title: "_DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA"
author: windows-sdk-content
description: Specifies the pixel aspect ratio (PAR) for the source and destination rectangles.
old-location: mf\dxvahd_stream_state_aspect_ratio_data.htm
tech.root: medfound
ms.assetid: dd7ab16e-2dc6-462e-b55d-b93a14c362cf
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure [Media Foundation], PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure pointer [Media Foundation], _DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, dxvahd/DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, dxvahd/PDXVAHD_STREAM_STATE_ASPECT_RATIO_DATA, mf.dxvahd_stream_state_aspect_ratio_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA
req.redist: 
---

# _DXVAHD_STREAM_STATE_ASPECT_RATIO_DATA structure


## -description


Specifies the pixel aspect ratio (PAR) for the source and destination rectangles.


## -struct-fields




### -field Enable

<b>If TRUE</b>, the <b>SourceAspectRatio</b> and <b>DestinationAspectRatio</b> members contain valid values<b></b>. Otherwise, the pixel aspect ratios are unspecified.


### -field SourceAspectRatio

A <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure that contains the source PAR. The default state value is 1:1 (square pixels).


### -field DestinationAspectRatio

A <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure that contains the destination PAR. The default state value is 1:1 (square pixels).


## -remarks



Pixel aspect ratios of the form 0/<i>n</i> and <i>n</i>/0 are not valid.

If the <b>Enable</b> member is <b>FALSE</b>, the device ignores the values of <b>SourceAspectRatio</b> and <b>DestinationAspectRatio</b>. 




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/384bdeaa-5360-42af-9f95-b791af2dcafc">Picture Aspect Ratio</a>
 

 

