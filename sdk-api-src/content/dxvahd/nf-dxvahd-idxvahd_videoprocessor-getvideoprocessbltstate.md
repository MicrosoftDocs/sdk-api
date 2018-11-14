---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.GetVideoProcessBltState
title: IDXVAHD_VideoProcessor::GetVideoProcessBltState
author: windows-sdk-content
description: Gets the value of a state parameter for blit operations performed by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_videoprocessor_getvideoprocessbltstate.htm
tech.root: medfound
ms.assetid: 5fdb0d39-7a64-41fd-8f70-4085ddbc7ebc
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetVideoProcessBltState, GetVideoProcessBltState method [Media Foundation], GetVideoProcessBltState method [Media Foundation],IDXVAHD_VideoProcessor interface, IDXVAHD_VideoProcessor interface [Media Foundation],GetVideoProcessBltState method, IDXVAHD_VideoProcessor.GetVideoProcessBltState, IDXVAHD_VideoProcessor::GetVideoProcessBltState, dxvahd/IDXVAHD_VideoProcessor::GetVideoProcessBltState, mf.idxvahd_videoprocessor_getvideoprocessbltstate
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
 - IDXVAHD_VideoProcessor.GetVideoProcessBltState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxvahd.h
: 
- IDXVAHD_VideoProcessor.GetVideoProcessBltState
: 
---

# IDXVAHD_VideoProcessor::GetVideoProcessBltState


## -description


Gets the value of a state parameter for blit operations performed by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param State [in]

The state parameter to query, specified as a member of the <a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a> enumeration.


### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pData [out]

A pointer to a buffer allocated by the caller. The method copies the state data into the buffer. The buffer must be large enough to hold the data structure that corresponds to the state parameter. For more information, see <a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a>
 

 

