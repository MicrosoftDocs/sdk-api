---
UID: NF:dxvahd.IDXVAHD_Device.CreateVideoProcessor
title: IDXVAHD_Device::CreateVideoProcessor (dxvahd.h)
description: Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["CreateVideoProcessor","CreateVideoProcessor method [Media Foundation]","CreateVideoProcessor method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","CreateVideoProcessor method","IDXVAHD_Device.CreateVideoProcessor","IDXVAHD_Device::CreateVideoProcessor","dxvahd/IDXVAHD_Device::CreateVideoProcessor","mf.idxvahd_device_createvideoprocessor"]
old-location: mf\idxvahd_device_createvideoprocessor.htm
tech.root: mf
ms.assetid: 903e2c05-e4d4-42ca-a28d-6d4738ae6cfc
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessor, CreateVideoProcessor method [Media Foundation], CreateVideoProcessor method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],CreateVideoProcessor method, IDXVAHD_Device.CreateVideoProcessor, IDXVAHD_Device::CreateVideoProcessor, dxvahd/IDXVAHD_Device::CreateVideoProcessor, mf.idxvahd_device_createvideoprocessor
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
 - IDXVAHD_Device::CreateVideoProcessor
 - dxvahd/IDXVAHD_Device::CreateVideoProcessor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.CreateVideoProcessor
---

# IDXVAHD_Device::CreateVideoProcessor


## -description

Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -parameters

### -param pVPGuid [in]

A GUID that identifies the video processor to create. This GUID must equal the value of the <b>VPGuid</b> member from one of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps">DXVAHD_VPCAPS</a> structures retrieved by the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">IDXVAHD_Device::GetVideoProcessorCaps</a> method.

### -param ppVideoProcessor [out]

Receives a pointer to the <a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>