---
UID: NC:dxvahd.PDXVAHDSW_CreateVideoProcessor
title: PDXVAHDSW_CreateVideoProcessor (dxvahd.h)
description: Creates a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor plug-in.
helpviewer_keywords: ["PDXVAHDSW_CreateVideoProcessor","PDXVAHDSW_CreateVideoProcessor callback","PDXVAHDSW_CreateVideoProcessor callback function [Media Foundation]","dxvahd/PDXVAHDSW_CreateVideoProcessor","mf.pdxvahdsw_createvideoprocessor"]
old-location: mf\pdxvahdsw_createvideoprocessor.htm
tech.root: mf
ms.assetid: 69ddcfc4-e91a-4ad5-ac0f-41683352d55a
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_CreateVideoProcessor, PDXVAHDSW_CreateVideoProcessor callback, PDXVAHDSW_CreateVideoProcessor callback function [Media Foundation], dxvahd/PDXVAHDSW_CreateVideoProcessor, mf.pdxvahdsw_createvideoprocessor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDXVAHDSW_CreateVideoProcessor
 - dxvahd/PDXVAHDSW_CreateVideoProcessor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_CreateVideoProcessor
---

# PDXVAHDSW_CreateVideoProcessor callback function


## -description

Creates a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor plug-in.

## -parameters

### -param hDevice [in]

A handle to the plug-in DXVA-HD device that creates the video processor.

### -param pVPGuid [in]

A GUID that identifies the video processor to create.

### -param phVideoProcessor [out]

Receives a handle to the software video processor.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor">IDXVAHD_Device::CreateVideoProcessor</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
