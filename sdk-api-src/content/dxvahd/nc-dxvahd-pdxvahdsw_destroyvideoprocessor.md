---
UID: NC:dxvahd.PDXVAHDSW_DestroyVideoProcessor
title: PDXVAHDSW_DestroyVideoProcessor
author: windows-driver-content
description: Destroys a sofware Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\pdxvahdsw_destroyvideoprocessor.htm
old-project: medfound
ms.assetid: 46667a66-3638-4cf0-9966-3e659d00f914
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PDXVAHDSW_DestroyVideoProcessor, PDXVAHDSW_DestroyVideoProcessor function pointer [Media Foundation], dxvahd/PDXVAHDSW_DestroyVideoProcessor, mf.pdxvahdsw_destroyvideoprocessor
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
-	PDXVAHDSW_DestroyVideoProcessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PDXVAHDSW_DestroyVideoProcessor callback


## -description


Destroys a sofware Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.


## -returns



If this function pointer succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

