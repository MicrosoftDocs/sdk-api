---
UID: NN:segment.IMSVidAudioRendererDevices
title: IMSVidAudioRendererDevices (segment.h)
description: The IMSVidAudioRendererDevices interface represents a collection of audio renderers. Applications can use this interface to enumerate the collection. The MSVidAudioRendererDevices object exposes this method.
old-location: mstv\imsvidaudiorendererdevices.htm
tech.root: mstv
ms.assetid: 2cf03260-7abe-4602-8364-447d076a4f76
ms.date: 12/05/2018
ms.keywords: IMSVidAudioRendererDevices, IMSVidAudioRendererDevices interface [Microsoft TV Technologies], IMSVidAudioRendererDevices interface [Microsoft TV Technologies],described, IMSVidAudioRendererDevicesInterface, mstv.imsvidaudiorendererdevices, segment/IMSVidAudioRendererDevices
ms.topic: interface
f1_keywords:
- segment/IMSVidAudioRendererDevices
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidAudioRendererDevices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidAudioRendererDevices interface


## -description



The <b>IMSVidAudioRendererDevices</b> interface represents a collection of audio renderers. Applications can use this interface to enumerate the collection. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695116(v=vs.85)">MSVidAudioRendererDevices</a> object exposes this method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAudioRendererDevices</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidAudioRendererDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidAudioRendererDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorendererdevices-add">Add</a>
</td>
<td align="left" width="63%">
Adds an audio renderer to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorendererdevices-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorendererdevices-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorendererdevices-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidaudiorendererdevices-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAudioRendererDevices)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

