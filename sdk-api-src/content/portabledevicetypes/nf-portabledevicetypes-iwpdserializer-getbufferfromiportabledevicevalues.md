---
UID: NF:portabledevicetypes.IWpdSerializer.GetBufferFromIPortableDeviceValues
title: IWpdSerializer::GetBufferFromIPortableDeviceValues method
author: windows-driver-content
description: The GetBufferFromIPortableDeviceValues method serializes a submitted IPortableDeviceValues interface to an allocated byte array. The byte array returned is allocated for the caller and should be freed by the caller using CoTaskMemFree.
old-location: wpdsdk\iwpdserializer_getbufferfromiportabledevicevalues.htm
old-project: wpd_sdk
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetBufferFromIPortableDeviceValues method [Windows Portable Devices SDK], GetBufferFromIPortableDeviceValues method [Windows Portable Devices SDK], IWpdSerializer interface, GetBufferFromIPortableDeviceValues,IWpdSerializer.GetBufferFromIPortableDeviceValues, IWpdSerializer, IWpdSerializer interface [Windows Portable Devices SDK], GetBufferFromIPortableDeviceValues method, IWpdSerializer::GetBufferFromIPortableDeviceValues, IWpdSerializerGetBufferFromIPortableDeviceValues, portabledevicetypes/IWpdSerializer::GetBufferFromIPortableDeviceValues, wpdsdk.iwpdserializer_getbufferfromiportabledevicevalues
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
-	IWpdSerializer.GetBufferFromIPortableDeviceValues
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWpdSerializer::GetBufferFromIPortableDeviceValues method


## -description



The <b>GetBufferFromIPortableDeviceValues</b> method serializes a submitted <b>IPortableDeviceValues</b> interface to an allocated byte array. The byte array returned is allocated for the caller and should be freed by the caller using <b>CoTaskMemFree</b>.




## -parameters




### -param pSource [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface to serialize.


### -param ppBuffer [out]

Pointer to a <b>BYTE*</b> that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling <b>CoTaskMemFree</b>.


### -param pdwBufferSize [out]

Pointer to a <b>DWORD</b> that specifies the size of allocated buffer, in bytes.


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
There was not enough memory available to create the buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/837bd850-6e27-4f8e-a612-d16f61b92b1d">IWpdSerializer Interface</a>
 

 

