---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderConfigurations
title: IDirectXVideoDecoderService::GetDecoderConfigurations (dxva2api.h)
author: windows-sdk-content
description: Gets the configurations that are available for a decoder device.
old-location: mf\idirectxvideodecoderservice_getdecoderconfigurations.htm
tech.root: medfound
ms.assetid: 7d2c24f3-9066-4e8b-aad6-98b7245088a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7d2c24f3-9066-4e8b-aad6-98b7245088a5, GetDecoderConfigurations, GetDecoderConfigurations method [Media Foundation], GetDecoderConfigurations method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],GetDecoderConfigurations method, IDirectXVideoDecoderService.GetDecoderConfigurations, IDirectXVideoDecoderService::GetDecoderConfigurations, dxva2api/IDirectXVideoDecoderService::GetDecoderConfigurations, mf.idirectxvideodecoderservice_getdecoderconfigurations
ms.topic: method
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - dxva2api.h
api_name:
 - IDirectXVideoDecoderService.GetDecoderConfigurations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoDecoderService::GetDecoderConfigurations


## -description


Gets the configurations that are available for a decoder device.
        


## -parameters




### -param Guid [in]

A GUID that identifies the decoder device. To get the available device GUIDs, call <a href="https://msdn.microsoft.com/53980b1f-2be1-4267-a581-a4b09255b89f">IDirectXVideoDecoderService::GetDecoderDeviceGuids</a>.
          


### -param pVideoDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.
          


### -param pReserved [in]

Reserved. Set to <b>NULL</b>.
          


### -param pCount [out]

Receives the number of configurations.
          


### -param ppConfigs [out]

Receives an array of <a href="https://msdn.microsoft.com/1515cfa9-24ff-4c65-adca-f4143d36685c">DXVA2_ConfigPictureDecode</a> structures. The size of the array is retrieved in the <i>pCount</i> parameter. The caller must free the memory for the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b> if you simply want the number of configurations (returned in <i>pCount</i>) but not the GUIDs.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1515cfa9-24ff-4c65-adca-f4143d36685c">DXVA2_ConfigPictureDecode</a>



<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
 

 

