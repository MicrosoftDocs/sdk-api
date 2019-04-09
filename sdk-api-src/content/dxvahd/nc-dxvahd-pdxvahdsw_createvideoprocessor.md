---
UID: NC:dxvahd.PDXVAHDSW_CreateVideoProcessor
title: PDXVAHDSW_CreateVideoProcessor (dxvahd.h)
author: windows-sdk-content
description: Creates a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor plug-in.
old-location: mf\pdxvahdsw_createvideoprocessor.htm
tech.root: medfound
ms.assetid: 69ddcfc4-e91a-4ad5-ac0f-41683352d55a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_CreateVideoProcessor, PDXVAHDSW_CreateVideoProcessor callback, PDXVAHDSW_CreateVideoProcessor callback function [Media Foundation], dxvahd/PDXVAHDSW_CreateVideoProcessor, mf.pdxvahdsw_createvideoprocessor
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
 - PDXVAHDSW_CreateVideoProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_CreateVideoProcessor callback function


## -description


Creates a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor plug-in.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device that creates the video processor.


### -param *pVPGuid [in]

A GUID that identifies the video processor to create.


### -param *phVideoProcessor [out]

Receives a handle to the software video processor.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/903e2c05-e4d4-42ca-a28d-6d4738ae6cfc">IDXVAHD_Device::CreateVideoProcessor</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

