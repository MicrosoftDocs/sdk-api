---
UID: NN:segment.IMSVidDevice
title: IMSVidDevice (segment.h)
description: The IMSVidDevice interface is the base interface for all the devices and features that the Video Control supports.helpviewer_keywords: ["IMSVidDevice","IMSVidDevice interface [Microsoft TV Technologies]","IMSVidDevice interface [Microsoft TV Technologies]","described","IMSVidDeviceInterface","mstv.imsviddevice","segment/IMSVidDevice"]
old-location: mstv\imsviddevice.htm
tech.root: mstv
ms.assetid: 5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef
ms.date: 12/05/2018
ms.keywords: IMSVidDevice, IMSVidDevice interface [Microsoft TV Technologies], IMSVidDevice interface [Microsoft TV Technologies],described, IMSVidDeviceInterface, mstv.imsviddevice, segment/IMSVidDevice
f1_keywords:
- segment/IMSVidDevice
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
- IMSVidDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidDevice interface


## -description



The <b>IMSVidDevice</b> interface is the base interface for all the devices and features that the Video Control supports.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidDevice</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get__category">get__Category</a>
</td>
<td align="left" width="63%">
Retrieves the category of the device as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get__classid">get__ClassID</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the device as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get_category">get_Category</a>
</td>
<td align="left" width="63%">
Retrieves the category of the device as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get_classid">get_ClassID</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the device as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get_power">get_Power</a>
</td>
<td align="left" width="63%">
Retrieves the power status of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-get_status">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves status information about the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-isequaldevice">IsEqualDevice</a>
</td>
<td align="left" width="63%">
Queries whether this device and another device represent the same underlying hardware

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsviddevice-put_power">put_Power</a>
</td>
<td align="left" width="63%">
Turns the device on or off.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidDevice)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

