---
UID: NS:dxvahd._DXVAHD_CONTENT_DESC
title: "_DXVAHD_CONTENT_DESC"
author: windows-sdk-content
description: Describes a video stream for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\dxvahd_content_desc.htm
tech.root: medfound
ms.assetid: 9319a98d-8f43-4f29-8787-18dec53dff88
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DXVAHD_CONTENT_DESC, DXVAHD_CONTENT_DESC structure [Media Foundation], _DXVAHD_CONTENT_DESC, dxvahd/DXVAHD_CONTENT_DESC, mf.dxvahd_content_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DXVAHD_CONTENT_DESC
product: Windows
targetos: Windows
req.typenames: DXVAHD_CONTENT_DESC
req.redist: 
---

# _DXVAHD_CONTENT_DESC structure


## -description


Describes a video stream for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

The display driver can use the information in this structure to optimize the capabilities of the video processor. For example, some capabilities might not be exposed for high-definition (HD) content, for performance reasons. 


## -struct-fields




### -field InputFrameFormat

A member of the <a href="https://msdn.microsoft.com/fc720dd3-e9c1-4b92-ac09-8e53cff44bec">DXVAHD_FRAME_FORMAT</a> enumeration that describes how the video stream is interlaced.


### -field InputFrameRate

The frame rate of the input video stream, specified as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure.


### -field InputWidth

The width of the input frames, in pixels.


### -field InputHeight

The height of the input frames, in pixels.


### -field OutputFrameRate

The frame rate of the output video stream, specified as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure.


### -field OutputWidth

The width of the output frames, in pixels.


### -field OutputHeight

The height of the output frames, in pixels.


## -remarks



Frame rates are expressed as ratios. For example, 30 frames per second (fps) is expressed as 30:1, and 29.97 fps is expressed as 30000/1001. For interlaced content, a frame consists of two fields, so that the frame rate is half the field rate.
      

 If the application will composite two or more input streams, use the largest stream for the values of <b>InputWidth</b> and <b>InputHeight</b>.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

