---
UID: NN:portabledeviceapi.IPortableDevicePropertiesBulk
title: IPortableDevicePropertiesBulk (portabledeviceapi.h)
author: windows-sdk-content
description: The IPortableDevicePropertiesBulk interface queries or sets multiple properties on multiple objects on a device, asynchronously.
old-location: wpdsdk\iportabledevicepropertiesbulk.htm
tech.root: wpd_sdk
ms.assetid: 57cda40a-8573-4b6c-981e-770f35186038
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulk, IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK], IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesBulkInterface, portabledeviceapi/IPortableDevicePropertiesBulk, wpdsdk.iportabledevicepropertiesbulk
ms.topic: interface
f1_keywords: 
 - "portabledeviceapi/IPortableDevicePropertiesBulk"
dev_langs:
 - c++
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevicePropertiesBulk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDevicePropertiesBulk interface


## -description



The <b>IPortableDevicePropertiesBulk</b> interface queries or sets multiple properties on multiple objects on a device, asynchronously. Information is returned by an application-implemented <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback</a> interface.

To get this interface, call <b>QueryInterface</b> on <b>IPortableDeviceProperties</b>. If the device does not support bulk operations, this call will fail with E_NOINTERFACE.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevicePropertiesBulk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDevicePropertiesBulk</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending properties request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat">QueueGetValuesByObjectFormat</a>
</td>
<td align="left" width="63%">
Queues a request for properties of objects of a specific format on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist">QueueGetValuesByObjectList</a>
</td>
<td align="left" width="63%">
Queues a request for one or more specified properties from one or more specified objects on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist">QueueSetValuesByObjectList</a>
</td>
<td align="left" width="63%">
Queues a request to set one or more specified values on one or more specified objects on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">Start</a>
</td>
<td align="left" width="63%">
Starts a queued operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 

