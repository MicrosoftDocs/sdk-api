---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.SetVideoProcessBltState
title: IDXVAHD_VideoProcessor::SetVideoProcessBltState (dxvahd.h)
author: windows-sdk-content
description: Sets a state parameter for a blit operation by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_videoprocessor_setvideoprocessbltstate.htm
tech.root: medfound
ms.assetid: adc08662-7977-402d-9eb1-505333550fc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXVAHD_VideoProcessor interface [Media Foundation],SetVideoProcessBltState method, IDXVAHD_VideoProcessor.SetVideoProcessBltState, IDXVAHD_VideoProcessor::SetVideoProcessBltState, SetVideoProcessBltState, SetVideoProcessBltState method [Media Foundation], SetVideoProcessBltState method [Media Foundation],IDXVAHD_VideoProcessor interface, dxvahd/IDXVAHD_VideoProcessor::SetVideoProcessBltState, mf.idxvahd_videoprocessor_setvideoprocessbltstate
ms.topic: method
f1_keywords: 
 - "dxvahd/IDXVAHD_VideoProcessor.SetVideoProcessBltState"
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
 - IDXVAHD_VideoProcessor.SetVideoProcessBltState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXVAHD_VideoProcessor::SetVideoProcessBltState


## -description


Sets a state parameter for a blit operation by a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param State [in]

The state parameter to set, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-_dxvahd_blt_state">DXVAHD_BLT_STATE</a> enumeration.


### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pData [in]

A pointer to a buffer that contains the state data. The meaning of the data depends on the <i>State</i> parameter. Each state has a corresponding data structure; for more information, see <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-_dxvahd_blt_state">DXVAHD_BLT_STATE</a>. The caller allocates the buffer and fills in the parameter data before calling this method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>
 

 

