---
UID: NF:portabledevicetypes.IWpdSerializer.WriteIPortableDeviceValuesToBuffer
title: IWpdSerializer::WriteIPortableDeviceValuesToBuffer method
author: windows-driver-content
description: The WriteIPortableDeviceValuesToBuffer method serializes an IPortableDeviceValues interface to a caller-allocated byte array.
old-location: wpdsdk\iwpdserializer_writeiportabledevicevaluestobuffer.htm
old-project: wpd_sdk
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWpdSerializer, IWpdSerializer interface [Windows Portable Devices SDK], WriteIPortableDeviceValuesToBuffer method, IWpdSerializer::WriteIPortableDeviceValuesToBuffer, IWpdSerializerWriteIPortableDeviceValuesToBuffer, WriteIPortableDeviceValuesToBuffer method [Windows Portable Devices SDK], WriteIPortableDeviceValuesToBuffer method [Windows Portable Devices SDK], IWpdSerializer interface, WriteIPortableDeviceValuesToBuffer,IWpdSerializer.WriteIPortableDeviceValuesToBuffer, portabledevicetypes/IWpdSerializer::WriteIPortableDeviceValuesToBuffer, wpdsdk.iwpdserializer_writeiportabledevicevaluestobuffer
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
-	IWpdSerializer.WriteIPortableDeviceValuesToBuffer
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWpdSerializer::WriteIPortableDeviceValuesToBuffer method


## -description



The <b>WriteIPortableDeviceValuesToBuffer</b> method serializes an <b>IPortableDeviceValues</b> interface to a caller-allocated byte array.




## -parameters




### -param dwOutputBufferLength [in]

<b>DWORD</b> that specifies the size of <i>pBuffer</i>, in bytes.


### -param pResults [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface to serialize.


### -param pBuffer [out]

Pointer to a caller-allocated buffer. To learn the size of the required buffer, call <b>GetSerializedSize</b>.


### -param pdwBytesWritten [out]

Pointer to a <b>DWORD</b> that indicates the number of bytes that was actually written to the caller-allocated buffer.


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
The caller-provided buffer was not big enough.

</td>
</tr>
</table>
 




## -remarks



This method copies an <b>IPortableDeviceValues</b> interface into an existing buffer. If you want to allocate a new buffer, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff597644">GetBufferFromIPortableDeviceValues</a>.




## -see-also




<a href="https://msdn.microsoft.com/837bd850-6e27-4f8e-a612-d16f61b92b1d">IWpdSerializer Interface</a>
 

 

