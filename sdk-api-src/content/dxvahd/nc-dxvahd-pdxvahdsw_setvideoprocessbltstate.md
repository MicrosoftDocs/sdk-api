---
UID: NC:dxvahd.PDXVAHDSW_SetVideoProcessBltState
title: PDXVAHDSW_SetVideoProcessBltState (dxvahd.h)
author: windows-sdk-content
description: Sets a state parameter for blit operations by a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_setvideoprocessbltstate.htm
tech.root: medfound
ms.assetid: 604af2f8-42e8-465c-a49f-8c6c9bcc84dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_SetVideoProcessBltState, PDXVAHDSW_SetVideoProcessBltState callback, PDXVAHDSW_SetVideoProcessBltState callback function [Media Foundation], dxvahd/PDXVAHDSW_SetVideoProcessBltState, mf.pdxvahdsw_setvideoprocessbltstate
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
 - PDXVAHDSW_SetVideoProcessBltState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_SetVideoProcessBltState callback function


## -description


Sets a state parameter for blit operations by a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param State [in]

The state parameter to set, specified as a member of the <a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a> enumeration.


### -param DataSize [in]

The size of the buffer pointed to by <i>pData</i>, in bytes.




### -param *pData [in]

A pointer to a buffer that contains the state data. 


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

