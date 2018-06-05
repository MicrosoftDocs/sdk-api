---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.SetVideoProcessStreamState
title: IDXVAHD_VideoProcessor::SetVideoProcessStreamState
author: windows-sdk-content
description: Sets a state parameter for an input stream on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_videoprocessor_setvideoprocessstreamstate.htm
old-project: medfound
ms.assetid: 40a8444f-576e-40ff-804e-0912812f0ee6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IDXVAHD_VideoProcessor interface [Media Foundation],SetVideoProcessStreamState method, IDXVAHD_VideoProcessor.SetVideoProcessStreamState, IDXVAHD_VideoProcessor::SetVideoProcessStreamState, SetVideoProcessStreamState, SetVideoProcessStreamState method [Media Foundation], SetVideoProcessStreamState method [Media Foundation],IDXVAHD_VideoProcessor interface, dxvahd/IDXVAHD_VideoProcessor::SetVideoProcessStreamState, mf.idxvahd_videoprocessor_setvideoprocessstreamstate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxvahd.h
api_name:
-	IDXVAHD_VideoProcessor.SetVideoProcessStreamState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXVAHD_VideoProcessor::SetVideoProcessStreamState


## -description


Sets a state parameter for an input stream on a  Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param StreamNumber [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


### -param State [in]

The state parameter to set, specified as a member of the <a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a> enumeration.


### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pData [in]

A pointer to a buffer that contains the state data. The meaning of the data depends on the <i>State</i> parameter. Each state has a corresponding data structure; for more information, see <a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>. The caller allocates the buffer and fills in the parameter data before calling this method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        Call this method to set state parameters that apply to individual input streams. 
      




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a>
 

 

