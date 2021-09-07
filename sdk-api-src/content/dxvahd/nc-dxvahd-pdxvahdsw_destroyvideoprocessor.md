---
UID: NC:dxvahd.PDXVAHDSW_DestroyVideoProcessor
title: PDXVAHDSW_DestroyVideoProcessor (dxvahd.h)
description: Destroys a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["PDXVAHDSW_DestroyVideoProcessor","PDXVAHDSW_DestroyVideoProcessor callback","PDXVAHDSW_DestroyVideoProcessor callback function [Media Foundation]","dxvahd/PDXVAHDSW_DestroyVideoProcessor","mf.pdxvahdsw_destroyvideoprocessor"]
old-location: mf\pdxvahdsw_destroyvideoprocessor.htm
tech.root: mf
ms.assetid: 46667a66-3638-4cf0-9966-3e659d00f914
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_DestroyVideoProcessor, PDXVAHDSW_DestroyVideoProcessor callback, PDXVAHDSW_DestroyVideoProcessor callback function [Media Foundation], dxvahd/PDXVAHDSW_DestroyVideoProcessor, mf.pdxvahdsw_destroyvideoprocessor
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
 - PDXVAHDSW_DestroyVideoProcessor
 - dxvahd/PDXVAHDSW_DestroyVideoProcessor
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
 - PDXVAHDSW_DestroyVideoProcessor
---

# PDXVAHDSW_DestroyVideoProcessor callback function


## -description

Destroys a software Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -parameters

### -param hVideoProcessor [in]

A handle to the software DXVA-HD video processor.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>