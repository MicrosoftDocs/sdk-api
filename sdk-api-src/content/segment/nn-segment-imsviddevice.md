---
UID: NN:segment.IMSVidDevice
title: IMSVidDevice
author: windows-sdk-content
description: The IMSVidDevice interface is the base interface for all the devices and features that the Video Control supports.
old-location: mstv\imsviddevice.htm
tech.root: mstv
ms.assetid: 5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidDevice, IMSVidDevice interface [Microsoft TV Technologies], IMSVidDevice interface [Microsoft TV Technologies],described, IMSVidDeviceInterface, mstv.imsviddevice, segment/IMSVidDevice
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
 - IMSVidDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidDevice interface


## -description



The <b>IMSVidDevice</b> interface is the base interface for all the devices and features that the Video Control supports.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidDevice</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMSVidDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2c5023ee-f38b-48c7-907d-363ca70bf94f">get__Category</a>
</td>
<td align="left" width="63%">
Retrieves the category of the device as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80890372-2d92-4a3a-963f-2a6ca6632c52">get__ClassID</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the device as a <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/369080c6-b707-494e-a663-e78e7d8d3eaf">get_Category</a>
</td>
<td align="left" width="63%">
Retrieves the category of the device as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78910e3d-bd00-48c5-b1be-504dc92280a0">get_ClassID</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the device as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb484684-7c20-498d-939e-ae5964d35669">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the friendly name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3be4247b-43d4-4a32-8643-7eb2637aee6f">get_Power</a>
</td>
<td align="left" width="63%">
Retrieves the power status of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b11df7f3-d227-4c74-89a3-90716b3b3a12">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves status information about the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f59466-7a2a-453e-999c-c7ebf126d18b">IsEqualDevice</a>
</td>
<td align="left" width="63%">
Queries whether this device and another device represent the same underlying hardware

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a0122a8-6015-4255-a7d6-ab72b4025bd6">put_Power</a>
</td>
<td align="left" width="63%">
Turns the device on or off.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidDevice)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

