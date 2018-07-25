---
UID: NN:segment.IMSVidOutputDevices
title: IMSVidOutputDevices
author: windows-sdk-content
description: The IMSVidOutputDevices interface represents a collection of output devices.Output devices include video and audio renderers, and the Stream Buffer Sink object.
old-location: mstv\imsvidoutputdevices.htm
old-project: mstv
ms.assetid: 54776225-ad60-450b-99b4-851cae60ffa7
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidOutputDevices, IMSVidOutputDevices interface [Microsoft TV Technologies], IMSVidOutputDevices interface [Microsoft TV Technologies],described, IMSVidOutputDevicesInterface, mstv.imsvidoutputdevices, segment/IMSVidOutputDevices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidOutputDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidOutputDevices interface


## -description



The <b>IMSVidOutputDevices</b> interface represents a collection of output devices.

Output devices include video and audio renderers, and the Stream Buffer Sink object. To obtain the audio and video renders, you can use the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/4ac78904-18ca-4bcb-9c0e-15595a756ecd">IMSVidCtl::get_AudioRendererActive</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6ab81536-2701-408e-be3a-f44375ef8193">IMSVidCtl::get_AudioRenderersAvailable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0b69abaf-95ab-49b9-9555-a2244224cb5d">IMSVidCtl::get_VideoRendererActive</a>
</li>
<li>
<a href="https://msdn.microsoft.com/20e5b2f3-33ea-4b0d-84b8-e4b0b61e0348">IMSVidCtl::get_VideoRenderersAvailable</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidOutputDevices</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMSVidOutputDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidOutputDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an output device to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f2203bb-9367-4713-8369-06002a5842e9">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4da44cb-84cb-46ae-9898-993802c9bfac">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/373dd785-3671-4afa-92ac-e61a39a68228">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidOutputDevices)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

