---
UID: NF:mfidl.IMFSensorDevice.GetDeviceAttributes
title: IMFSensorDevice::GetDeviceAttributes
author: windows-driver-content
description: Gets the IMFAttributes for the sensor group.
old-location: mf\imfsensordevice_getdeviceattributes.htm
old-project: medfound
ms.assetid: 4F509D34-23C3-4034-8D89-0A2E0651F235
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetDeviceAttributes, GetDeviceAttributes method [Media Foundation], GetDeviceAttributes method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetDeviceAttributes method, IMFSensorDevice.GetDeviceAttributes, IMFSensorDevice::GetDeviceAttributes, mf.imfsensordevice_getdeviceattributes, mfidl/IMFSensorDevice::GetDeviceAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorDevice.GetDeviceAttributes
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorDevice::GetDeviceAttributes


## -description


Gets the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> for the sensor group. 


## -parameters




### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface representing the internal attribute store of the sensor device.


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

                The <i>ppAttributes</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

                The sensor device has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The object returned is a copy of the internal attribute store and so changes made to the returned attributes have no effect on the <a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

