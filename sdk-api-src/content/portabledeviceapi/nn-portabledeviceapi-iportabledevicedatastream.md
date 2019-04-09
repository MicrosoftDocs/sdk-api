---
UID: NN:portabledeviceapi.IPortableDeviceDataStream
title: IPortableDeviceDataStream (portabledeviceapi.h)
author: windows-sdk-content
description: The IPortableDeviceDataStream interface exposes additional methods on an IStream that is used for data transfers.
old-location: wpdsdk\iportabledevicedatastream.htm
tech.root: wpd_sdk
ms.assetid: d7bd955a-886f-4081-bfc3-cd2d7e2cfb24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceDataStream, IPortableDeviceDataStream interface [Windows Portable Devices SDK], IPortableDeviceDataStream interface [Windows Portable Devices SDK],described, IPortableDeviceDataStreamInterface, portabledeviceapi/IPortableDeviceDataStream, wpdsdk.iportabledevicedatastream
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
 - IPortableDeviceDataStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceDataStream interface


## -description



The <b>IPortableDeviceDataStream</b> interface exposes additional methods on an <b>IStream</b> that is used for data transfers. It is obtained by calling <b>QueryInterface</b> on the <b>IStream</b> that is retrieved by <a href="https://msdn.microsoft.com/d5c9a85a-59fa-4b7b-acc7-d450ecd10593">IPortableDeviceResources::GetStream</a> or <a href="https://msdn.microsoft.com/ea3445cc-69af-40a6-a5a4-695e0f2e1fb6">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceDataStream</b> interface inherits from <b>IStream</b>. <b>IPortableDeviceDataStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceDataStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a86cc78-8ef8-45e1-b63a-dac4c9dcdd9c">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a call in progress on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd506e52-723d-4a3c-b73e-425700ccd3ec">GetObjectID</a>
</td>
<td align="left" width="63%">
Retrieves the object ID of the resource that was written to the device.

</td>
</tr>
</table> 

