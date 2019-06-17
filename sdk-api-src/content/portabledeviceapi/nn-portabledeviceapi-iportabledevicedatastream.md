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
f1_keywords: ["portabledeviceapi/IPortableDeviceDataStream"]
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
ms.custom: 19H1
---

# IPortableDeviceDataStream interface


## -description



The <b>IPortableDeviceDataStream</b> interface exposes additional methods on an <b>IStream</b> that is used for data transfers. It is obtained by calling <b>QueryInterface</b> on the <b>IStream</b> that is retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getstream">IPortableDeviceResources::GetStream</a> or <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a>.




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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicedatastream-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a call in progress on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicedatastream-getobjectid">GetObjectID</a>
</td>
<td align="left" width="63%">
Retrieves the object ID of the resource that was written to the device.

</td>
</tr>
</table> 

