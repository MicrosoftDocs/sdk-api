---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.GetVideoProcessStreamState
title: IDXVAHD_VideoProcessor::GetVideoProcessStreamState
author: windows-sdk-content
description: Gets the value of a state parameter for an input stream on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_videoprocessor_getvideoprocessstreamstate.htm
tech.root: MedFound
ms.assetid: 1ceeae95-d67d-4f11-b815-f4eef517e7ce
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetVideoProcessStreamState, GetVideoProcessStreamState method [Media Foundation], GetVideoProcessStreamState method [Media Foundation],IDXVAHD_VideoProcessor interface, IDXVAHD_VideoProcessor interface [Media Foundation],GetVideoProcessStreamState method, IDXVAHD_VideoProcessor.GetVideoProcessStreamState, IDXVAHD_VideoProcessor::GetVideoProcessStreamState, dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessStreamState, mf.idxvahd_videoprocessor_getvideoprocessstreamstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor.GetVideoProcessStreamState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXVAHD_VideoProcessor::GetVideoProcessStreamState


## -description


Gets the value of a state parameter for an input stream on a  Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param StreamNumber [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


### -param State [in]

The state parameter to query, specified as a member of the <a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a> enumeration.


### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pData [out]

A pointer to a buffer allocated by the caller. The method copies the state data into the buffer. The buffer must be large enough to hold the data structure that corresponds to the state parameter. For more information, see <a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a>
 

 

