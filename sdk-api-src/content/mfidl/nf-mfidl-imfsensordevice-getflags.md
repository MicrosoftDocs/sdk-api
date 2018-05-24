---
UID: NF:mfidl.IMFSensorDevice.GetFlags
title: IMFSensorDevice::GetFlags
author: windows-driver-content
description: Gets the flags set for the sensor device. This method is reserved for future use.
old-location: mf\imfsensordevice_getflags.htm
old-project: medfound
ms.assetid: 802649EE-7A24-429A-92DB-775A215BCD79
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetFlags method, IMFSensorDevice.GetFlags, IMFSensorDevice::GetFlags, mf.imfsensordevice_getflags, mfidl/IMFSensorDevice::GetFlags
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
-	IMFSensorDevice.GetFlags
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorDevice::GetFlags


## -description


Gets the flags set for the sensor device. This method is reserved for future use.


## -parameters




### -param pFlags [out]

The flags set for the sensor device.


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

                The <i>pDeviceId</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

                The sensor group has not been initialized.

</td>
</tr>
</table>
 




## -remarks



This method is reserved for future use and should not be called.




## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

