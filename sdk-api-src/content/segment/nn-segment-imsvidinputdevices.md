---
UID: NN:segment.IMSVidInputDevices
title: IMSVidInputDevices
author: windows-sdk-content
description: The IMSVidInputDevices interface represents a collection of input devices. The MSVidInputDevices object exposes this object.
old-location: mstv\imsvidinputdevices.htm
old-project: mstv
ms.assetid: cb9d9885-718e-43b9-b195-66149bd7e973
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMSVidInputDevices, IMSVidInputDevices interface [Microsoft TV Technologies], IMSVidInputDevices interface [Microsoft TV Technologies],described, IMSVidInputDevicesInterface, mstv.imsvidinputdevices, segment/IMSVidInputDevices
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
 - IMSVidInputDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidInputDevices interface


## -description



The <b>IMSVidInputDevices</b> interface represents a collection of input devices. The <a href="https://msdn.microsoft.com/cae86bb2-8633-49cf-a03d-e20f50d0fdfd">MSVidInputDevices</a> object exposes this object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidInputDevices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidInputDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidInputDevices</b> interface has these methods.
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
Adds an input device to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a33c9549-c5a6-48c1-bf49-66a7bf81cdaa">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52c2d9a1-f688-4f5e-a120-082d70f8dff1">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d8b2d88-e591-4280-966b-9c23f05d55f9">get_Item</a>
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



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidInputDevices)</code>.




## -see-also




<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

