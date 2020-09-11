---
UID: NN:control.IBasicVideo
title: IBasicVideo (control.h)
description: The IBasicVideo interface sets video properties such as the destination and source rectangles.
helpviewer_keywords: ["IBasicVideo","IBasicVideo interface [DirectShow]","IBasicVideo interface [DirectShow]","described","IBasicVideoInterface","control/IBasicVideo","dshow.ibasicvideo"]
old-location: dshow\ibasicvideo.htm
tech.root: dshow
ms.assetid: 14f45bdc-2271-459d-b165-c860c8fc3e0b
ms.date: 12/05/2018
ms.keywords: IBasicVideo, IBasicVideo interface [DirectShow], IBasicVideo interface [DirectShow],described, IBasicVideoInterface, control/IBasicVideo, dshow.ibasicvideo
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicVideo
 - control/IBasicVideo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo
---

# IBasicVideo interface


## -description

The <code>IBasicVideo</code> interface sets video properties such as the destination and source rectangles. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and Video Mixing Renderer filters implement this interface, but the interface is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.

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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicVideo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBasicVideo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_avgtimeperframe">get_AvgTimePerFrame</a>
</td>
<td align="left" width="63%">
Retrieves the average time between successive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_biterrorrate">get_BitErrorRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit error rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_bitrate">get_BitRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_destinationheight">get_DestinationHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_destinationleft">get_DestinationLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_destinationtop">get_DestinationTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_destinationwidth">get_DestinationWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceheight">get_SourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourceleft">get_SourceLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcetop">get_SourceTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_sourcewidth">get_SourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_videoheight">get_VideoHeight</a>
</td>
<td align="left" width="63%">
Retrieves the video height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-get_videowidth">get_VideoWidth</a>
</td>
<td align="left" width="63%">
Retrieves the video width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-getcurrentimage">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Returns a copy of the current image that is waiting at the renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-getdestinationposition">GetDestinationPosition</a>
</td>
<td align="left" width="63%">
Retrieves the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-getsourceposition">GetSourcePosition</a>
</td>
<td align="left" width="63%">
Retrieves the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-getvideopaletteentries">GetVideoPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves the color palette entries required by the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-getvideosize">GetVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the native video dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-isusingdefaultdestination">IsUsingDefaultDestination</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-isusingdefaultsource">IsUsingDefaultSource</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationheight">put_DestinationHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationleft">put_DestinationLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationtop">put_DestinationTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationwidth">put_DestinationWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_sourceheight">put_SourceHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_sourceleft">put_SourceLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_sourcetop">put_SourceTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_sourcewidth">put_SourceWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-setdefaultdestinationposition">SetDefaultDestinationPosition</a>
</td>
<td align="left" width="63%">
Reverts to the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-setdefaultsourceposition">SetDefaultSourcePosition</a>
</td>
<td align="left" width="63%">
Reverts to the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-setdestinationposition">SetDestinationPosition</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-setsourceposition">SetSourcePosition</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

