---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats
title: IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats
author: windows-sdk-content
description: Gets a list of substream formats supported by a specified video processor device.
old-location: mf\idirectxvideoprocessorservice_getvideoprocessorsubstreamformats.htm
tech.root: medfound
ms.assetid: 10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 10ad4d8d-9b5e-4f77-8244-c29a0e14a5b1, GetVideoProcessorSubStreamFormats, GetVideoProcessorSubStreamFormats method [Media Foundation], GetVideoProcessorSubStreamFormats method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorSubStreamFormats method, IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats, IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats, mf.idirectxvideoprocessorservice_getvideoprocessorsubstreamformats
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectXVideoProcessorService.GetVideoProcessorSubStreamFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats


## -description


Gets a list of substream formats supported by a specified video processor device.
        


## -parameters




### -param VideoProcDeviceGuid [in]

A GUID that identifies the video processor device. 
          To get the list of video processor GUIDs, call <a href="https://msdn.microsoft.com/26b52407-7c75-4731-aff3-41376aa9ac3a">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.


### -param pVideoDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a> structure that describes the video content.
          


### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="https://msdn.microsoft.com/bea4835d-fd7f-4ac3-8466-7f4e0d799a12">Video FOURCCs</a>.
          


### -param pCount [out]

Receives the number of elements returned in the <i>ppFormats</i> array.
          


### -param pFormats

TBD




#### - ppFormats [out]

Receives an array of <b>D3DFORMAT</b> values. The caller must free the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. The array can contain both RGB and YUB pixel formats.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a>
 

 

