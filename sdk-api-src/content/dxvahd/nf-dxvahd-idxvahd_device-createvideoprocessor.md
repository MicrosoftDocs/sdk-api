---
UID: NF:dxvahd.IDXVAHD_Device.CreateVideoProcessor
title: IDXVAHD_Device::CreateVideoProcessor
author: windows-sdk-content
description: Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\idxvahd_device_createvideoprocessor.htm
tech.root: medfound
ms.assetid: 903e2c05-e4d4-42ca-a28d-6d4738ae6cfc
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateVideoProcessor, CreateVideoProcessor method [Media Foundation], CreateVideoProcessor method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],CreateVideoProcessor method, IDXVAHD_Device.CreateVideoProcessor, IDXVAHD_Device::CreateVideoProcessor, dxvahd/IDXVAHD_Device::CreateVideoProcessor, mf.idxvahd_device_createvideoprocessor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.CreateVideoProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxvahd.h
: 
- IDXVAHD_Device.CreateVideoProcessor
: 
---

# IDXVAHD_Device::CreateVideoProcessor


## -description


Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -parameters




### -param pVPGuid [in]

A GUID that identifies the video processor to create. This GUID must equal the value of the <b>VPGuid</b> member from one of the <a href="https://msdn.microsoft.com/25ec6802-ca6e-42d4-b1d5-de7597e3d042">DXVAHD_VPCAPS</a> structures retrieved by the <a href="https://msdn.microsoft.com/d9423b3f-4a4b-49f0-8018-c19a7b663300">IDXVAHD_Device::GetVideoProcessorCaps</a> method.


### -param ppVideoProcessor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a>
 

 

