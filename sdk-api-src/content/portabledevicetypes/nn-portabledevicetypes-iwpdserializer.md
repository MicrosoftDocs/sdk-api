---
UID: NN:portabledevicetypes.IWpdSerializer
title: IWpdSerializer
author: windows-driver-content
description: The IWpdSerializer interface is used by the device driver to serialize IPortableDeviceValues interfaces to and from the raw data buffers used to communicate with the application.Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling IPortableDevice::SendCommand.To get this interface, call CoCreateInstance and pass in IID_IWpdSerializer.
old-location: wpdsdk\iwpdserializer.htm
old-project: wpd_sdk
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWpdSerializer, IWpdSerializer interface [Windows Portable Devices SDK], IWpdSerializer interface [Windows Portable Devices SDK], described, IWpdSerializerInterface, portabledevicetypes/IWpdSerializer, wpdsdk.iwpdserializer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: portabledevicetypes.h
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
req.typenames: WPD_STREAM_UNITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IWpdSerializer
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWpdSerializer interface


## -description



The <b>IWpdSerializer</b> interface is used by the device driver to serialize <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interfaces to and from the raw data buffers used to communicate with the application.

Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling <a href="https://msdn.microsoft.com/ccc7f87a-dea3-4a1e-a181-86928e23bd35">IPortableDevice::SendCommand</a>.

To get this interface, call <b>CoCreateInstance</b> and pass in <b>IID_IWpdSerializer</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWpdSerializer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWpdSerializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWpdSerializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597644">GetBufferFromIPortableDeviceValues</a>
</td>
<td align="left" width="63%">
Serializes a submitted <b>IPortableDeviceValues</b> interface to an allocated byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597645">GetIPortableDeviceValuesFromBuffer</a>
</td>
<td align="left" width="63%">
Deserializes a byte array to an <b>IPortableDeviceValues</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597646">GetSerializedSize</a>
</td>
<td align="left" width="63%">
Calculates the buffer size that is required to hold a serialized <b>IPortableDeviceValues</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597647">WriteIPortableDeviceValuesToBuffer</a>
</td>
<td align="left" width="63%">
Serializes an <b>IPortableDeviceValues</b> interface to a caller-allocated byte array.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597566">Driver Interfaces</a>
 

 

