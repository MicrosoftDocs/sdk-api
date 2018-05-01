---
UID: NC:dxvahd.PDXVAHDSW_SetVideoProcessStreamState
title: PDXVAHDSW_SetVideoProcessStreamState
author: windows-driver-content
description: Sets a state parameter for an input stream on a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_setvideoprocessstreamstate.htm
old-project: medfound
ms.assetid: 1fbecdbd-9f04-4d1e-82a6-4c6ce522cdaf
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PDXVAHDSW_SetVideoProcessStreamState, PDXVAHDSW_SetVideoProcessStreamState function pointer [Media Foundation], dxvahd/PDXVAHDSW_SetVideoProcessStreamState, mf.pdxvahdsw_setvideoprocessstreamstate
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
req.typenames: DXVA_COPPStatusSignalingCmdData
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	dxvahd.h
api_name:
-	PDXVAHDSW_SetVideoProcessStreamState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PDXVAHDSW_SetVideoProcessStreamState callback


## -description


Sets a state parameter for an input stream on a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param StreamNumber [in]

The zero-based index of the input stream.


### -param State [in]

The state parameter to set, specified as a member of the <a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a> enumeration.




### -param DataSize [in]

The size of the buffer pointed to by <i>pData</i>, in bytes.




### -param *pData [in]

A pointer to a buffer that contains the state data.


## -returns



If this function pointer succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

