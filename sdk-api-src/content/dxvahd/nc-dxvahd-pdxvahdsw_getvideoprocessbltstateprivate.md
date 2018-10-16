---
UID: NC:dxvahd.PDXVAHDSW_GetVideoProcessBltStatePrivate
title: PDXVAHDSW_GetVideoProcessBltStatePrivate
author: windows-sdk-content
description: Gets a private blit state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_getvideoprocessbltstateprivate.htm
tech.root: medfound
ms.assetid: 32154457-5270-4e60-a16c-bca72c6a9673
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: PDXVAHDSW_GetVideoProcessBltStatePrivate, PDXVAHDSW_GetVideoProcessBltStatePrivate callback, PDXVAHDSW_GetVideoProcessBltStatePrivate callback function [Media Foundation], dxvahd/PDXVAHDSW_GetVideoProcessBltStatePrivate, mf.pdxvahdsw_getvideoprocessbltstateprivate
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
 - PDXVAHDSW_GetVideoProcessBltStatePrivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_GetVideoProcessBltStatePrivate callback function


## -description


Gets a private blit state from a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


### -param *pData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/b85d4429-9346-4c85-8c3d-efffe0c1e63a">DXVAHD_BLT_STATE_PRIVATE_DATA</a> structure. On input, the <b>Guid</b> member specifies the private state to query. On output, the structure contains the state information.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/5fdb0d39-7a64-41fd-8f70-4085ddbc7ebc">IDXVAHD_VideoProcessor::GetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

