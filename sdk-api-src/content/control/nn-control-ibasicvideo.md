---
UID: NN:control.IBasicVideo
title: IBasicVideo
author: windows-sdk-content
description: The IBasicVideo interface sets video properties such as the destination and source rectangles.
old-location: dshow\ibasicvideo.htm
old-project: DirectShow
ms.assetid: 14f45bdc-2271-459d-b165-c860c8fc3e0b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IBasicVideo, IBasicVideo interface [DirectShow], IBasicVideo interface [DirectShow],described, IBasicVideoInterface, control/IBasicVideo, dshow.ibasicvideo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: control.h
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IBasicVideo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBasicVideo interface


## -description



The <code>IBasicVideo</code> interface sets video properties such as the destination and source rectangles. The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter and Video Mixing Renderer filters implement this interface, but the interface is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.

The <code>IBasicVideo</code> interface manipulates the following rectangles associated with the video image:

<ul>
<li>The <i>source</i> rectangle is the portion of the original image that gets displayed.</li>
<li>The <i>destination</i> rectangle is the portion of the video window the receives the source rectangle.</li>
<li>The <i>video</i> rectangle is the original video image.</li>
</ul>
In other words, the video renderer crops the image to the source rectangle, and then stretches or shrinks the cropped image to the destination rectangle. All rectangle dimensions are given in pixels.

Properties set on the Video Renderer persist between successive connections and disconnections.

<b>Error codes</b>: If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicVideo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IBasicVideo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBasicVideo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a32a1a46-cde3-401a-b933-c72e399e9ea1">get_AvgTimePerFrame</a>
</td>
<td align="left" width="63%">
Retrieves the average time between successive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c61b8a96-83ea-49e2-884e-c9fb3526cc46">get_BitErrorRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit error rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aae4c41d-4cab-4c49-9733-44ba5e0e03bb">get_BitRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21d6c74a-2adb-4015-b0df-5acb26c22212">get_DestinationHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/578f5bbd-23b0-4100-a1d8-0987381fd56f">get_DestinationLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79690655-ac84-4119-9d87-799990424f00">get_DestinationTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e27bb57-ca88-4478-86b8-250a69f5fc78">get_DestinationWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f4e779a-cfa9-496d-a021-d24ae3daa5b3">get_SourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea64dae-d643-44c1-9026-f9b0dcd25ef1">get_SourceLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87ad3699-5a1b-4fa0-b7bd-5ec87758e9fa">get_SourceTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c6f7e01-5f93-4277-b664-c5be0ea42004">get_SourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/872d26e5-b765-4c1f-b494-45df39f06a41">get_VideoHeight</a>
</td>
<td align="left" width="63%">
Retrieves the video height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5167b1e-1341-43b0-bc72-e990ee76e3c4">get_VideoWidth</a>
</td>
<td align="left" width="63%">
Retrieves the video width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e7fbf27-3519-4c02-b785-98e29902df65">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Returns a copy of the current image that is waiting at the renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee2abf52-edc2-471e-bf9b-eda04f2eabe4">GetDestinationPosition</a>
</td>
<td align="left" width="63%">
Retrieves the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4624e38c-63ff-4860-a899-c70e44e0f8aa">GetSourcePosition</a>
</td>
<td align="left" width="63%">
Retrieves the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a022bc5-56f5-41c0-940f-f9074791a353">GetVideoPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves the color palette entries required by the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbabba8b-b86b-451b-ad06-4454174ee352">GetVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the native video dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eceec24b-7743-4989-b112-e6a70283d397">IsUsingDefaultDestination</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85cb633f-95cd-4cbe-9572-324ec784e6bb">IsUsingDefaultSource</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e530bf39-d352-4808-9ac6-5e3d322e1905">put_DestinationHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/718fcc07-1e37-4e37-ab99-39f629e65309">put_DestinationLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/254fb104-c080-411d-9795-edcd4da41bdc">put_DestinationTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ae22194-19ca-4a20-9b4f-d9f39e346606">put_DestinationWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8cb4ae1-cbbf-44cb-9387-770ee95280a1">put_SourceHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0388d5fe-5434-41b9-b005-c0e4bf36bb27">put_SourceLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a76518d-f79d-45ef-8e19-a3e5ee1e4db0">put_SourceTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0747a1fb-42b6-452f-8a92-eb87931c004c">put_SourceWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82ee1be5-4a58-4104-a8a5-3c3926e2f1d2">SetDefaultDestinationPosition</a>
</td>
<td align="left" width="63%">
Reverts to the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7b440c0-8f91-4f32-adc6-82fa658125d0">SetDefaultSourcePosition</a>
</td>
<td align="left" width="63%">
Reverts to the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e638eb33-5a7f-4ebc-910f-72566e251f17">SetDestinationPosition</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afe78775-f2b0-4d10-a702-f0329fe79c6d">SetSourcePosition</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

