---
UID: NN:portabledeviceapi.IPortableDevicePropertiesBulk
title: IPortableDevicePropertiesBulk
author: windows-sdk-content
description: The IPortableDevicePropertiesBulk interface queries or sets multiple properties on multiple objects on a device, asynchronously.
old-location: wpdsdk\iportabledevicepropertiesbulk.htm
old-project: wpd_sdk
ms.assetid: 57cda40a-8573-4b6c-981e-770f35186038
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDevicePropertiesBulk, IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK], IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesBulkInterface, portabledeviceapi/IPortableDevicePropertiesBulk, wpdsdk.iportabledevicepropertiesbulk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevicePropertiesBulk
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDevicePropertiesBulk interface


## -description



The <b>IPortableDevicePropertiesBulk</b> interface queries or sets multiple properties on multiple objects on a device, asynchronously. Information is returned by an application-implemented <a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback</a> interface.

To get this interface, call <b>QueryInterface</b> on <b>IPortableDeviceProperties</b>. If the device does not support bulk operations, this call will fail with E_NOINTERFACE.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevicePropertiesBulk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDevicePropertiesBulk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDevicePropertiesBulk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending properties request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a52b45b5-fd9b-4af5-bb82-293816190e38">QueueGetValuesByObjectFormat</a>
</td>
<td align="left" width="63%">
Queues a request for properties of objects of a specific format on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c29777c-4125-46a1-94b2-8d70374e566a">QueueGetValuesByObjectList</a>
</td>
<td align="left" width="63%">
Queues a request for one or more specified properties from one or more specified objects on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfb03354-e395-4fb7-aa76-a1f786ccd71c">QueueSetValuesByObjectList</a>
</td>
<td align="left" width="63%">
Queues a request to set one or more specified values on one or more specified objects on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts a queued operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

