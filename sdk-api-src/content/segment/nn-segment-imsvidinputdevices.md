---
UID: NN:segment.IMSVidInputDevices
title: IMSVidInputDevices (segment.h)
author: windows-sdk-content
description: The IMSVidInputDevices interface represents a collection of input devices. The MSVidInputDevices object exposes this object.
old-location: mstv\imsvidinputdevices.htm
tech.root: mstv
ms.assetid: cb9d9885-718e-43b9-b195-66149bd7e973
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidInputDevices, IMSVidInputDevices interface [Microsoft TV Technologies], IMSVidInputDevices interface [Microsoft TV Technologies],described, IMSVidInputDevicesInterface, mstv.imsvidinputdevices, segment/IMSVidInputDevices
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
 - IMSVidInputDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidInputDevices interface


## -description



The <b>IMSVidInputDevices</b> interface represents a collection of input devices. The <a href="https://msdn.microsoft.com/cae86bb2-8633-49cf-a03d-e20f50d0fdfd">MSVidInputDevices</a> object exposes this object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidInputDevices</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMSVidInputDevices</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd694571(v=VS.85).aspx">Add</a>
</td>
<td align="left" width="63%">
Adds an input device to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694574(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694572(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694573(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694575(v=VS.85).aspx">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidInputDevices)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

