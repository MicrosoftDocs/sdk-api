---
UID: NN:wiavideo.IWiaVideo
title: IWiaVideo
author: windows-sdk-content
description: The IWiaVideo interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.Note  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use DirectShow to acquire images from video.
old-location: wia\_wia_IWiaVideo.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\iwiavideo.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWiaVideo, IWiaVideo interface [WIA], IWiaVideo interface [WIA],described, _wia_IWiaVideo, wia._wia_IWiaVideo, wiavideo/IWiaVideo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wiavideo.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaVideo interface


## -description


The <b>IWiaVideo</b> interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.


<div class="alert"><b>Note</b>  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use <a href="http://msdn.microsoft.com/en-us/library/ms783323(VS.85).aspx">DirectShow</a> to acquire images from video.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaVideo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaVideo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0ea7ab75-7893-485d-a523-faa6019e1f67">CreateVideoByDevNum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0ea7ab75-7893-485d-a523-faa6019e1f67">IWiaVideo::CreateVideoByDevNum</a> method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ea34408-cf71-45d2-ac3b-6e3ad9622ae5">CreateVideoByName</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4ea34408-cf71-45d2-ac3b-6e3ad9622ae5">IWiaVideo::CreateVideoByName</a> method creates a connection to a streaming video device with the friendly device name obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc5379fb-54ba-4bcd-b302-e07676885106">CreateVideoByWiaDevID</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bc5379fb-54ba-4bcd-b302-e07676885106">IWiaVideo::CreateVideoByWiaDevID</a> method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c175fb1-8d3f-47a5-98d6-8f7d256b8f4e">DestroyVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9c175fb1-8d3f-47a5-98d6-8f7d256b8f4e">IWiaVideo::DestroyVideo</a> method shuts down the streaming video. To restart video playback, the application must call one of the <b>IWiaVideo</b> CreateVideo methods again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccd5abb6-8baa-4751-a8f8-5120c78739b4">GetCurrentState</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ccd5abb6-8baa-4751-a8f8-5120c78739b4">IWiaVideo::GetCurrentState</a> method specifies the state of the video stream as a member of the <a href="https://msdn.microsoft.com/3d460ca8-6760-4649-b33d-ebf24d318346">WIAVIDEO_STATE</a> enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ed4c5669-33e4-43f9-8e61-7cd2b01fdd44">IWiaVideo::Pause</a> method pauses video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8917c5f-6569-496d-a2ed-bd5ed76dfbcf">Play</a>
</td>
<td align="left" width="63%">
Begins playback of streaming video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08a22af1-73cf-4d05-8242-8c7f1497a15b">ResizeVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/08a22af1-73cf-4d05-8242-8c7f1497a15b">IWiaVideo::ResizeVideo</a> method resizes the video playback to the largest supported resolution that fits inside the parent window. Call this method whenever the parent window is moved or resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edd4b242-f4df-4f5b-8655-e697e78fef47">TakePicture</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/edd4b242-f4df-4f5b-8655-e697e78fef47">IWiaVideo::TakePicture</a> method extracts a still image from the video stream, and saves the image as a JPEG file.

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

<a href="https://msdn.microsoft.com/f7bff8d2-1cdd-4d32-877b-c61343888a26">ImagesDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f7bff8d2-1cdd-4d32-877b-c61343888a26">IWiaVideo::ImagesDirectory</a> property specifies the full path and directory where images are stored when calling the <a href="https://msdn.microsoft.com/edd4b242-f4df-4f5b-8655-e697e78fef47">IWiaVideo::TakePicture</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c2a8b794-94f8-4405-878a-5c257c33affc">PreviewVisible</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c2a8b794-94f8-4405-878a-5c257c33affc">IWiaVideo::PreviewVisible</a> property specifies whether the video playback is visible in its parent window. This does not affect the <a href="https://msdn.microsoft.com/3d460ca8-6760-4649-b33d-ebf24d318346">WIAVIDEO_STATE</a> of the video.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaVideo</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



