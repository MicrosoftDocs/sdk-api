---
UID: NF:portabledevicetypes.IWpdSerializer.GetIPortableDeviceValuesFromBuffer
title: IWpdSerializer::GetIPortableDeviceValuesFromBuffer method
author: windows-driver-content
description: The GetIPortableDeviceValuesFromBuffer method deserializes a byte array to an IPortableDeviceValues interface.
old-location: wpdsdk\iwpdserializer_getiportabledevicevaluesfrombuffer.htm
old-project: wpd_sdk
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetIPortableDeviceValuesFromBuffer method [Windows Portable Devices SDK], GetIPortableDeviceValuesFromBuffer method [Windows Portable Devices SDK], IWpdSerializer interface, GetIPortableDeviceValuesFromBuffer,IWpdSerializer.GetIPortableDeviceValuesFromBuffer, IWpdSerializer, IWpdSerializer interface [Windows Portable Devices SDK], GetIPortableDeviceValuesFromBuffer method, IWpdSerializer::GetIPortableDeviceValuesFromBuffer, IWpdSerializerGetIPortableDeviceValuesFromBuffer, portabledevicetypes/IWpdSerializer::GetIPortableDeviceValuesFromBuffer, wpdsdk.iwpdserializer_getiportabledevicevaluesfrombuffer
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
-	IWpdSerializer.GetIPortableDeviceValuesFromBuffer
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWpdSerializer::GetIPortableDeviceValuesFromBuffer method


## -description



The <b>GetIPortableDeviceValuesFromBuffer</b> method deserializes a byte array to an <b>IPortableDeviceValues</b> interface.




## -parameters




### -param pBuffer [in]

Pointer to the buffer to deserialize.


### -param dwInputBufferLength [in]

<b>DWORD</b> that specifies the size of the buffer, in bytes.


### -param ppParams [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface created from the buffer. The application is responsible for calling <b>Release</b> on the interface.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unspecified conversion error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/837bd850-6e27-4f8e-a612-d16f61b92b1d">IWpdSerializer Interface</a>
 

 

