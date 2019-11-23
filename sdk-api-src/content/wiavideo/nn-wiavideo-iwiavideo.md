---
UID: NN:wiavideo.IWiaVideo
title: IWiaVideo (wiavideo.h)

description: The IWiaVideo interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.Note  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use DirectShow to acquire images from video.
old-location: wia\_wia_IWiaVideo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\iwiavideo.htm

ms.date: 12/05/2018
ms.keywords: IWiaVideo, IWiaVideo interface [WIA], IWiaVideo interface [WIA],described, _wia_IWiaVideo, wia._wia_IWiaVideo, wiavideo/IWiaVideo
ms.topic: interface
f1_keywords: 
 - "wiavideo/IWiaVideo"
dev_langs:
 - c++
req.header: wiavideo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wiavideo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaVideo interface


## -description


The <b>IWiaVideo</b> interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.


<div class="alert"><b>Note</b>  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use <a href="https://docs.microsoft.com/previous-versions/ms783323(v=vs.85)">DirectShow</a> to acquire images from video.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaVideo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaVideo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWiaVideo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">CreateVideoByDevNum</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">IWiaVideo::CreateVideoByDevNum</a> method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">CreateVideoByName</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">IWiaVideo::CreateVideoByName</a> method creates a connection to a streaming video device with the friendly device name obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">CreateVideoByWiaDevID</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">IWiaVideo::CreateVideoByWiaDevID</a> method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-destroyvideo">DestroyVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-destroyvideo">IWiaVideo::DestroyVideo</a> method shuts down the streaming video. To restart video playback, the application must call one of the <b>IWiaVideo</b> CreateVideo methods again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-getcurrentstate">GetCurrentState</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-getcurrentstate">IWiaVideo::GetCurrentState</a> method specifies the state of the video stream as a member of the <a href="https://docs.microsoft.com/windows/win32/api/wiavideo/ne-wiavideo-wiavideo_state">WIAVIDEO_STATE</a> enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-pause">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-pause">IWiaVideo::Pause</a> method pauses video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-play">Play</a>
</td>
<td align="left" width="63%">
Begins playback of streaming video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-resizevideo">ResizeVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-resizevideo">IWiaVideo::ResizeVideo</a> method resizes the video playback to the largest supported resolution that fits inside the parent window. Call this method whenever the parent window is moved or resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">TakePicture</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">IWiaVideo::TakePicture</a> method extracts a still image from the video stream, and saves the image as a JPEG file.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaVideo</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory">ImagesDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory">IWiaVideo::ImagesDirectory</a> property specifies the full path and directory where images are stored when calling the <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">IWiaVideo::TakePicture</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_previewvisible">PreviewVisible</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_previewvisible">IWiaVideo::PreviewVisible</a> property specifies whether the video playback is visible in its parent window. This does not affect the <a href="https://docs.microsoft.com/windows/win32/api/wiavideo/ne-wiavideo-wiavideo_state">WIAVIDEO_STATE</a> of the video.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaVideo</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



