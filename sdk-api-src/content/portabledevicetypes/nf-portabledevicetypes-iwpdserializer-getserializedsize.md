---
UID: NF:portabledevicetypes.IWpdSerializer.GetSerializedSize
title: IWpdSerializer::GetSerializedSize method
author: windows-driver-content
description: The GetSerializedSize method calculates the buffer size that is required to hold a serialized IPortableDeviceValues interface.
old-location: wpdsdk\iwpdserializer_getserializedsize.htm
old-project: wpd_sdk
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetSerializedSize method [Windows Portable Devices SDK], GetSerializedSize method [Windows Portable Devices SDK], IWpdSerializer interface, GetSerializedSize,IWpdSerializer.GetSerializedSize, IWpdSerializer, IWpdSerializer interface [Windows Portable Devices SDK], GetSerializedSize method, IWpdSerializer::GetSerializedSize, IWpdSerializerGetSerializedSize, portabledevicetypes/IWpdSerializer::GetSerializedSize, wpdsdk.iwpdserializer_getserializedsize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IWpdSerializer.GetSerializedSize
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWpdSerializer::GetSerializedSize method


## -description



The <b>GetSerializedSize</b> method calculates the buffer size that is required to hold a serialized <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface.




## -parameters




### -param pSource [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface whose size you want to request.


### -param pdwSize [out]

Pointer to a <b>DWORD</b> that indicates the buffer size that is required to serialize <i>pSource</i>, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A required pointer argument was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough available memory to create the buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/837bd850-6e27-4f8e-a612-d16f61b92b1d">IWpdSerializer Interface</a>
 

 

