---
UID: NC:dxvahd.PDXVAHDSW_VideoProcessBltHD
title: PDXVAHDSW_VideoProcessBltHD
author: windows-sdk-content
description: Performs a video processing blit.
old-location: mf\pdxvahdsw_videoprocessblthd.htm
tech.root: medfound
ms.assetid: 94e6b59f-dd00-4d32-b1ca-a592a67cd0ec
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PDXVAHDSW_VideoProcessBltHD, PDXVAHDSW_VideoProcessBltHD callback, PDXVAHDSW_VideoProcessBltHD callback function [Media Foundation], dxvahd/PDXVAHDSW_VideoProcessBltHD, mf.pdxvahdsw_videoprocessblthd
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
 - PDXVAHDSW_VideoProcessBltHD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_VideoProcessBltHD callback function


## -description


Performs a video processing blit.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param *pOutputSurface [in]

A pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface that receives the blit.


### -param OutputFrame [in]

The frame number of the output video frame, indexed from zero.


### -param StreamCount [in]

The number of input streams to process. 




### -param *pStreams [in]

A pointer to an array of <a href="https://msdn.microsoft.com/95d74c87-5884-4004-926f-108e9bbb012d">DXVAHD_STREAM_DATA</a> structures that contain information about the input streams. The number of elements in the array is given in the <i>StreamCount</i> parameter.




## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/59c4deee-4ef2-4aba-8188-989904055e70">IDXVAHD_VideoProcessor::VideoProcessBltHD</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

