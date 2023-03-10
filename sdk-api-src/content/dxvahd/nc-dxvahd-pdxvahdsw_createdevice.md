---
UID: NC:dxvahd.PDXVAHDSW_CreateDevice
title: PDXVAHDSW_CreateDevice (dxvahd.h)
description: Creates an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["PDXVAHDSW_CreateDevice","PDXVAHDSW_CreateDevice callback","PDXVAHDSW_CreateDevice callback function [Media Foundation]","dxvahd/PDXVAHDSW_CreateDevice","mf.pdxvahdsw_createdevice"]
old-location: mf\pdxvahdsw_createdevice.htm
tech.root: mf
ms.assetid: f76539c8-13a8-4608-87a6-4947f5debb02
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_CreateDevice, PDXVAHDSW_CreateDevice callback, PDXVAHDSW_CreateDevice callback function [Media Foundation], dxvahd/PDXVAHDSW_CreateDevice, mf.pdxvahdsw_createdevice
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
 - PDXVAHDSW_CreateDevice
 - dxvahd/PDXVAHDSW_CreateDevice
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
 - PDXVAHDSW_CreateDevice
---

# PDXVAHDSW_CreateDevice callback function


## -description

Creates an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param pD3DDevice [in]

A pointer to the <b>IDirect3DDevice9Ex</b> interface of the Direct3D device.

### -param phDevice [out]

Receives a handle to the plug-in DXVA-HD device.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
