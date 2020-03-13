---
UID: NN:mfidl.IMFMediaSource
title: IMFMediaSource (mfidl.h)
description: Implemented by media source objects.
old-location: mf\imfmediasource.htm
tech.root: medfound
ms.assetid: 8b579f61-6fea-4b20-a051-7633fc01fa05
ms.date: 12/05/2018
ms.keywords: 8b579f61-6fea-4b20-a051-7633fc01fa05, IMFMediaSource, IMFMediaSource interface [Media Foundation], IMFMediaSource interface [Media Foundation],described, mf.imfmediasource, mfidl/IMFMediaSource
f1_keywords:
- mfidl/IMFMediaSource
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFMediaSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSource interface


## -description


Implemented by media source objects.

Media sources are objects that generate media data. For example, the data might come from a video file, a network stream, or a hardware device, such as a camera. Each media source contains one or more streams, and each stream delivers data of one type, such as audio or video.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSource</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFMediaSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">CreatePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the media source's presentation descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses all active streams in the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/remotecreatepresentationdescriptor">RemoteCreatePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">CreatePresentationDescriptor</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the media source and releases the resources it is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start">Start</a>
</td>
<td align="left" width="63%">
Starts, seeks, or restarts the media source by specifying where to start playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops all active streams in the media source.

</td>
</tr>
</table> 


## -remarks



In Windows 8, this interface is extended with <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex">IMFMediaSourceEx</a>.

For some device sources, such as cameras or microphones, the **IMFMediaSource** also implements the [IKsControl](https://docs.microsoft.com/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) which can be used by user mode applications to issue KSPROPERTY, KSEVENT and KSMETHOD operations to the underlying device driver.

> [!NOTE] 
> This interface is optional and may not be available. If this interface is not available, [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) will return E_NOINTERFACE. 



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-sources">Media Sources</a>
 

 

