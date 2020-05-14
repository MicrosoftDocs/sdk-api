---
UID: NF:evr.IMFVideoMixerControl.GetStreamZOrder
title: IMFVideoMixerControl::GetStreamZOrder (evr.h)
description: Retrieves the z-order of a video stream.helpviewer_keywords: ["9e0ba97c-c960-4e26-a89c-ea1a4e91e907","GetStreamZOrder","GetStreamZOrder method [Media Foundation]","GetStreamZOrder method [Media Foundation]","IMFVideoMixerControl interface","IMFVideoMixerControl interface [Media Foundation]","GetStreamZOrder method","IMFVideoMixerControl.GetStreamZOrder","IMFVideoMixerControl::GetStreamZOrder","evr/IMFVideoMixerControl::GetStreamZOrder","mf.imfvideomixercontrol_getstreamzorder"]
old-location: mf\imfvideomixercontrol_getstreamzorder.htm
tech.root: medfound
ms.assetid: 9e0ba97c-c960-4e26-a89c-ea1a4e91e907
ms.date: 12/05/2018
ms.keywords: 9e0ba97c-c960-4e26-a89c-ea1a4e91e907, GetStreamZOrder, GetStreamZOrder method [Media Foundation], GetStreamZOrder method [Media Foundation],IMFVideoMixerControl interface, IMFVideoMixerControl interface [Media Foundation],GetStreamZOrder method, IMFVideoMixerControl.GetStreamZOrder, IMFVideoMixerControl::GetStreamZOrder, evr/IMFVideoMixerControl::GetStreamZOrder, mf.imfvideomixercontrol_getstreamzorder
f1_keywords:
- evr/IMFVideoMixerControl.GetStreamZOrder
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoMixerControl.GetStreamZOrder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMixerControl::GetStreamZOrder


## -description



Retrieves the z-order of a video stream.




## -parameters




### -param dwStreamID [in]

Identifier of the stream. For the EVR media sink, the stream identifier is defined when the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> method is called. For the DirectShow EVR filter, the stream identifier corresponds to the pin index. The reference stream is always stream 0.


### -param pdwZ [out]

Receives the z-order value.


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideomixercontrol">IMFVideoMixerControl</a>
 

 

