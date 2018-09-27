---
UID: NN:segment.IMSVidVideoRendererDevices
title: IMSVidVideoRendererDevices
author: windows-sdk-content
description: The IMSVidVideoRendererDevices interface represents a collection of video renderers. The MSVidVideoRendererDevices object exposes this method. Applications can use this interface to enumerate the collection.
old-location: mstv\imsvidvideorendererdevices.htm
tech.root: MSTV
ms.assetid: cf8e1307-b4a5-464b-b9a6-32c195941309
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidVideoRendererDevices, IMSVidVideoRendererDevices interface [Microsoft TV Technologies], IMSVidVideoRendererDevices interface [Microsoft TV Technologies],described, IMSVidVideoRendererDevicesInterface, mstv.imsvidvideorendererdevices, segment/IMSVidVideoRendererDevices
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
 - IMSVidVideoRendererDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRendererDevices interface


## -description



The <b>IMSVidVideoRendererDevices</b> interface represents a collection of video renderers. The <a href="https://msdn.microsoft.com/f953f06b-48d2-404e-96b2-e7c0d1a38218">MSVidVideoRendererDevices</a> object exposes this method. Applications can use this interface to enumerate the collection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRendererDevices</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMSVidVideoRendererDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVideoRendererDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/650b7895-4e4b-494a-bc06-dafb67fca391">Add</a>
</td>
<td align="left" width="63%">
Adds a video renderer to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da321f4c-801a-4e27-bc82-5dab723adf97">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4308ed6a-b9c4-46f3-98eb-be23cd49c7dc">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cb169d2-f6b2-4156-aa11-f9b47437b731">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a1d8f8b-1e62-470d-8f94-afc238755cad">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRendererDevices)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

