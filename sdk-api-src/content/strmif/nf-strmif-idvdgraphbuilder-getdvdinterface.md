---
UID: NF:strmif.IDvdGraphBuilder.GetDvdInterface
title: IDvdGraphBuilder::GetDvdInterface method
author: windows-driver-content
description: The GetDvdInterface method retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.
old-location: dshow\idvdgraphbuilder_getdvdinterface.htm
old-project: DirectShow
ms.assetid: e16cb767-87a9-49f6-a3a7-88166f2abe73
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDvdInterface method [DirectShow], GetDvdInterface method [DirectShow], IDvdGraphBuilder interface, GetDvdInterface,IDvdGraphBuilder.GetDvdInterface, IDvdGraphBuilder, IDvdGraphBuilder interface [DirectShow], GetDvdInterface method, IDvdGraphBuilder::GetDvdInterface, IDvdGraphBuilderGetDvdInterface, dshow.idvdgraphbuilder_getdvdinterface, strmif/IDvdGraphBuilder::GetDvdInterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdGraphBuilder.GetDvdInterface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdGraphBuilder::GetDvdInterface method


## -description



The <b>GetDvdInterface</b> method retrieves interfaces from the DVD-Video playback graph to make DVD-Video playback development easier.




## -parameters




### -param riid [in]

IID of the requested interface.


### -param ppvIF [out]

Receives a pointer to the interface. The application must release the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppvIF</i> parameter is invalid. This parameter must not be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface could not be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_GRAPHNOTREADY</b></dt>
</dl>
</td>
<td width="60%">
The graph is not built yet. See Remarks.

</td>
</tr>
</table>
 




## -remarks



You can use this method to select and configure a video renderer filter before you build the filter graph for DVD playback. The following interfaces are available:

<ul>
<li><b>Overlay Mixer Filter</b>: <a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo</a>.</li>
<li><b>Video Mixing Renderer 7 (VMR-7)</b>: <a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig</a>, <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a>, <a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl</a>, and <a href="https://msdn.microsoft.com/02b4016b-a65b-41ac-b5c6-e5f6825f179c">IVMRMonitorConfig</a>.</li>
<li><b>Video Mixing Renderer 9 (VMR-9)</b>: <a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9</a>, <a href="https://msdn.microsoft.com/de48307a-3522-49a0-b0a5-73ce7cf90517">IVMRMixerBitmap9</a>, <a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9</a>, and <a href="https://msdn.microsoft.com/27a3a598-d8de-48b2-8b8c-6b5497db4c6c">IVMRMonitorConfig9</a>.</li>
<li><b>Enhanced Video Renderer (EVR)</b>: <a href="https://msdn.microsoft.com/13086d85-3dbf-4e9f-b065-d95e16412832">IEVRFilterConfig</a> and <a href="https://msdn.microsoft.com/70596630-5131-460f-9cb3-adcea201c3b2">IMFVideoRenderer</a>.<b>Windows Server 2003, Windows XP and Windows 2000:  </b>This interface is not supported.

</li>
</ul>
If you call <b>GetDvdInterface</b> to get any of these interfaces before you build the filter graph, the DVD Graph Builder creates the appropriate video renderer. It will use this renderer later when you build the graph. After the video renderer has been selected, you can no longer retrieve the interfaces for the other video renderers. (The <b>GetDvdInterface</b> method will return E_NOINTERFACE.)

Before the DVD playback graph is built, if you request any interfaces that are not on the previous list, the method returns VFW_E_DVD_GRAPHNOTREADY. To build the DVD graph, call <a href="https://msdn.microsoft.com/731d2f4b-2a54-451a-8d98-b5fdf47c1dc8">IDvdGraphBuilder::RenderDvdVideoVolume</a>. After you build the graph, you can use <b>GetDvdInterface</b> to retrieve some additional interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl</a> (deprecated), <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a>, <a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo</a> (deprecated), and <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> to control DVD playback.</li>
<li>
<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow</a>, <a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo</a>, and <a href="https://msdn.microsoft.com/a21fe7b9-75db-4c5b-bb29-42d305f048a1">IBasicVideo2</a> to control the video settings, in windowed mode only.</li>
<li>
<a href="https://msdn.microsoft.com/0335b263-8d32-4690-a606-ba2b3e382680">IBasicAudio</a> to control the audio settings.</li>
<li>
<a href="https://msdn.microsoft.com/b6fbb5c3-28af-4db6-8dc4-82271b69bf71">IAMLine21Decoder</a> to control closed caption display.</li>
<li>
<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig</a> and <a href="https://msdn.microsoft.com/d166b139-3ef7-4f47-817a-8f5b644a3776">IMixerPinConfig2</a> to configure the Overlay Mixer filter's first input pin, which delivers the primary video stream. (To get this interface for the other pins on the Overlay Mixer, enumerate the filter's pins and query them directly.) New applications should avoid using the Overlay Mixer filter.</li>
</ul>
To get other interfaces, call <a href="https://msdn.microsoft.com/1f12140b-d10d-47d9-8bac-33fab084bff4">IDvdGraphBuilder::GetFiltergraph</a>. Query the returned <b>IGraphBuilder</b> interface or use <b>EnumFilters</b> to enumerate the filters.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2179e54a-c6e2-4837-9f89-be210bde9180">IDvdGraphBuilder Interface</a>
 

 

