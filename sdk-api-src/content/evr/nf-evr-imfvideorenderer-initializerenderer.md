---
UID: NF:evr.IMFVideoRenderer.InitializeRenderer
title: IMFVideoRenderer::InitializeRenderer method
author: windows-driver-content
description: Sets a new mixer or presenter for the enhanced video renderer (EVR).
old-location: mf\imfvideorenderer_initializerenderer.htm
old-project: medfound
ms.assetid: e46a9596-9f3f-4430-8d45-bbc9c240be3b
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFVideoRenderer, IMFVideoRenderer interface [Media Foundation], InitializeRenderer method, IMFVideoRenderer::InitializeRenderer, InitializeRenderer method [Media Foundation], InitializeRenderer method [Media Foundation], IMFVideoRenderer interface, InitializeRenderer,IMFVideoRenderer.InitializeRenderer, e46a9596-9f3f-4430-8d45-bbc9c240be3b, evr/IMFVideoRenderer::InitializeRenderer, mf.imfvideorenderer_initializerenderer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: evr.h
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
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoRenderer.InitializeRenderer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoRenderer::InitializeRenderer method


## -description



Sets a new mixer or presenter for the enhanced video renderer (EVR).




## -parameters




### -param pVideoMixer [in]

Pointer to the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface of the mixer to use. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the EVR uses its default mixer.


### -param pVideoPresenter [in]

Pointer to the <a href="https://msdn.microsoft.com/8f6e3132-03e9-4a2e-9160-e39d29cf2408">IMFVideoPresenter</a> interface of the presenter to use. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the EVR uses its default presenter.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Either the mixer or the presenter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The mixer and presenter cannot be replaced in the current state. (EVR media sink.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
One or more input pins are connected. (DirectShow EVR filter.)

</td>
</tr>
</table>
 




## -remarks



Call this method directly after creating the EVR, before you do any of the following:

<ul>
<li>
Call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the EVR.

</li>
<li>
Call <a href="https://msdn.microsoft.com/72777c3d-b098-43b9-80ea-ef180b7f1a4a">IEVRFilterConfig::SetNumberOfStreams</a> on the EVR.

</li>
<li>
Connect any pins on the EVR filter, or set any media types on EVR media sink.

</li>
</ul>
The EVR filter returns VFW_E_WRONG_STATE if any of the filter's pins are connected. The EVR media sink returns MF_E_INVALIDREQUEST if a media type is set on any of the streams, or the presentation clock is running or paused.

The device identifiers for the mixer and the presenter must match. The <a href="https://msdn.microsoft.com/e23ebce0-be58-413a-ab71-d94811c96029">IMFVideoDeviceID::GetDeviceID</a> method returns the device identifier. If they do not match, the method returns E_INVALIDARG.

If the video renderer is in the protected media path (PMP), the mixer and presenter objects must be certified safe components and pass any trust authority verification that is being enforced. Otherwise, this method will fail.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/70596630-5131-460f-9cb3-adcea201c3b2">IMFVideoRenderer</a>
 

 

