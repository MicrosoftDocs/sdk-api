---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessStreamStatePrivate
title: PDXVAHDSW_GetVideoProcessStreamStatePrivate
author: windows-sdk-content
description: Gets a private stream state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_getvideoprocessstreamstateprivate.htm
tech.root: medfound
ms.assetid: db751314-8c3c-4969-87c4-0b2b2201ce20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PDXVAHDSW_GetVideoProcessStreamStatePrivate, PDXVAHDSW_GetVideoProcessStreamStatePrivate callback, PDXVAHDSW_GetVideoProcessStreamStatePrivate callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessStreamStatePrivate, mf.pdxvahdsw_getvideoprocessstreamstateprivate
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
 - PDXVAHDSW_GetVideoProcessStreamStatePrivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessStreamStatePrivate callback function


## -description


Gets a private stream state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param StreamNumber [in]

The zero-based index of the input stream.


### -param *pData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/3b7ce487-edec-4ff2-b971-72ddcc28162c">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure. On input, the <b>Guid</b> member specifies the private state to query. On output, the structure contains the state information.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/1ceeae95-d67d-4f11-b815-f4eef517e7ce">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

