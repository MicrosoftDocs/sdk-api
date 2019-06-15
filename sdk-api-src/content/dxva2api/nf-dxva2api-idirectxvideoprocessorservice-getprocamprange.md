---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetProcAmpRange
title: IDirectXVideoProcessorService::GetProcAmpRange (dxva2api.h)
author: windows-sdk-content
description: Gets the range of values for a video processor (ProcAmp) setting.
old-location: mf\idirectxvideoprocessorservice_getprocamprange.htm
tech.root: medfound
ms.assetid: b4945e2f-6907-4e02-9719-89c8e0bf1404
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProcAmpRange, GetProcAmpRange method [Media Foundation], GetProcAmpRange method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetProcAmpRange method, IDirectXVideoProcessorService.GetProcAmpRange, IDirectXVideoProcessorService::GetProcAmpRange, b4945e2f-6907-4e02-9719-89c8e0bf1404, dxva2api/IDirectXVideoProcessorService::GetProcAmpRange, mf.idirectxvideoprocessorservice_getprocamprange
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
 - IDirectXVideoProcessorService.GetProcAmpRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessorService::GetProcAmpRange


## -description


Gets the range of values for a video processor (ProcAmp) setting.
        


## -parameters




### -param VideoProcDeviceGuid [in]

A 
            GUID that identifies the video processor device.
          To get the list of video processor GUIDs, call <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids">IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids</a>.


### -param pVideoDesc [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ns-dxva2api-_dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.
          


### -param RenderTargetFormat [in]

The format of the render target surface, specified as a <b>D3DFORMAT</b> value. For more information, see the Direct3D documentation. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. See <a href="https://docs.microsoft.com/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.
          


### -param ProcAmpCap [in]

The 
            ProcAmp setting to query. See <a href="https://docs.microsoft.com/windows/desktop/medfound/procamp-settings">ProcAmp Settings</a>.
          


### -param pRange [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ns-dxva2api-_dxva2_valuerange">DXVA2_ValueRange</a> structure that receives the range of values for the setting specified in <i>ProcAmpCaps</i>.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>
 

 

