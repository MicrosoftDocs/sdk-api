---
UID: NN:control.IBasicVideo
title: IBasicVideo (control.h)
author: windows-sdk-content
description: The IBasicVideo interface sets video properties such as the destination and source rectangles.
old-location: dshow\ibasicvideo.htm
tech.root: DirectShow
ms.assetid: 14f45bdc-2271-459d-b165-c860c8fc3e0b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBasicVideo, IBasicVideo interface [DirectShow], IBasicVideo interface [DirectShow],described, IBasicVideoInterface, control/IBasicVideo, dshow.ibasicvideo
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicVideo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IBasicVideo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd389575(v=VS.85).aspx">get_AvgTimePerFrame</a>
</td>
<td align="left" width="63%">
Retrieves the average time between successive frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389576(v=VS.85).aspx">get_BitErrorRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit error rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389577(v=VS.85).aspx">get_BitRate</a>
</td>
<td align="left" width="63%">
Retrieves the approximate bit rate of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389578(v=VS.85).aspx">get_DestinationHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389579(v=VS.85).aspx">get_DestinationLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389580(v=VS.85).aspx">get_DestinationTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389581(v=VS.85).aspx">get_DestinationWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389582(v=VS.85).aspx">get_SourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389583(v=VS.85).aspx">get_SourceLeft</a>
</td>
<td align="left" width="63%">
Retrieves the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389584(v=VS.85).aspx">get_SourceTop</a>
</td>
<td align="left" width="63%">
Retrieves the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389585(v=VS.85).aspx">get_SourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389586(v=VS.85).aspx">get_VideoHeight</a>
</td>
<td align="left" width="63%">
Retrieves the video height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389587(v=VS.85).aspx">get_VideoWidth</a>
</td>
<td align="left" width="63%">
Retrieves the video width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389570(v=VS.85).aspx">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Returns a copy of the current image that is waiting at the renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389571(v=VS.85).aspx">GetDestinationPosition</a>
</td>
<td align="left" width="63%">
Retrieves the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389572(v=VS.85).aspx">GetSourcePosition</a>
</td>
<td align="left" width="63%">
Retrieves the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389573(v=VS.85).aspx">GetVideoPaletteEntries</a>
</td>
<td align="left" width="63%">
Retrieves the color palette entries required by the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389574(v=VS.85).aspx">GetVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the native video dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389588(v=VS.85).aspx">IsUsingDefaultDestination</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389589(v=VS.85).aspx">IsUsingDefaultSource</a>
</td>
<td align="left" width="63%">
Queries whether the renderer is using the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389590(v=VS.85).aspx">put_DestinationHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389591(v=VS.85).aspx">put_DestinationLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389592(v=VS.85).aspx">put_DestinationTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389593(v=VS.85).aspx">put_DestinationWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389594(v=VS.85).aspx">put_SourceHeight</a>
</td>
<td align="left" width="63%">
Sets the height of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389595(v=VS.85).aspx">put_SourceLeft</a>
</td>
<td align="left" width="63%">
Sets the x-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389596(v=VS.85).aspx">put_SourceTop</a>
</td>
<td align="left" width="63%">
Sets the y-coordinate of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389597(v=VS.85).aspx">put_SourceWidth</a>
</td>
<td align="left" width="63%">
Sets the width of the source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389598(v=VS.85).aspx">SetDefaultDestinationPosition</a>
</td>
<td align="left" width="63%">
Reverts to the default destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389599(v=VS.85).aspx">SetDefaultSourcePosition</a>
</td>
<td align="left" width="63%">
Reverts to the default source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389600(v=VS.85).aspx">SetDestinationPosition</a>
</td>
<td align="left" width="63%">
Sets the destination rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389601(v=VS.85).aspx">SetSourcePosition</a>
</td>
<td align="left" width="63%">
Sets the source rectangle.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

