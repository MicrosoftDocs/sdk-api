---
UID: NN:wiavideo.IWiaVideo
title: IWiaVideo (wiavideo.h)
author: windows-sdk-content
description: The IWiaVideo interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.Note  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use DirectShow to acquire images from video.
old-location: wia\_wia_IWiaVideo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\iwiavideo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaVideo, IWiaVideo interface [WIA], IWiaVideo interface [WIA],described, _wia_IWiaVideo, wia._wia_IWiaVideo, wiavideo/IWiaVideo
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/ms629884(v=VS.85).aspx">CreateVideoByDevNum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629884(v=VS.85).aspx">IWiaVideo::CreateVideoByDevNum</a> method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629886(v=VS.85).aspx">CreateVideoByName</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629886(v=VS.85).aspx">IWiaVideo::CreateVideoByName</a> method creates a connection to a streaming video device with the friendly device name obtained from a Directshow enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629889(v=VS.85).aspx">CreateVideoByWiaDevID</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629889(v=VS.85).aspx">IWiaVideo::CreateVideoByWiaDevID</a> method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629890(v=VS.85).aspx">DestroyVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629890(v=VS.85).aspx">IWiaVideo::DestroyVideo</a> method shuts down the streaming video. To restart video playback, the application must call one of the <b>IWiaVideo</b> CreateVideo methods again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629893(v=VS.85).aspx">GetCurrentState</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629893(v=VS.85).aspx">IWiaVideo::GetCurrentState</a> method specifies the state of the video stream as a member of the <a href="https://msdn.microsoft.com/en-us/library/ms630181(v=VS.85).aspx">WIAVIDEO_STATE</a> enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629898(v=VS.85).aspx">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629898(v=VS.85).aspx">IWiaVideo::Pause</a> method pauses video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629900(v=VS.85).aspx">Play</a>
</td>
<td align="left" width="63%">
Begins playback of streaming video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629903(v=VS.85).aspx">ResizeVideo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629903(v=VS.85).aspx">IWiaVideo::ResizeVideo</a> method resizes the video playback to the largest supported resolution that fits inside the parent window. Call this method whenever the parent window is moved or resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629905(v=VS.85).aspx">TakePicture</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629905(v=VS.85).aspx">IWiaVideo::TakePicture</a> method extracts a still image from the video stream, and saves the image as a JPEG file.

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

<a href="https://msdn.microsoft.com/en-us/library/ms629895(v=VS.85).aspx">ImagesDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629895(v=VS.85).aspx">IWiaVideo::ImagesDirectory</a> property specifies the full path and directory where images are stored when calling the <a href="https://msdn.microsoft.com/en-us/library/ms629905(v=VS.85).aspx">IWiaVideo::TakePicture</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms629902(v=VS.85).aspx">PreviewVisible</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629902(v=VS.85).aspx">IWiaVideo::PreviewVisible</a> property specifies whether the video playback is visible in its parent window. This does not affect the <a href="https://msdn.microsoft.com/en-us/library/ms630181(v=VS.85).aspx">WIAVIDEO_STATE</a> of the video.

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
 



