---
UID: NF:mfidl.IMFSensorDevice.GetDeviceType
title: IMFSensorDevice::GetDeviceType
author: windows-sdk-content
description: Gets a value that specifies the type of sensor device represented by the object.
old-location: mf\imfsensordevice_getdevicetype.htm
tech.root: medfound
ms.assetid: 6714B5A8-83F2-44CD-B061-749EA6BFBF20
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetDeviceType, GetDeviceType method [Media Foundation], GetDeviceType method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetDeviceType method, IMFSensorDevice.GetDeviceType, IMFSensorDevice::GetDeviceType, mf.imfsensordevice_getdevicetype, mfidl/IMFSensorDevice::GetDeviceType
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorDevice.GetDeviceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorDevice::GetDeviceType


## -description


Gets a value that specifies the type of sensor device represented by the object.


## -parameters




### -param pType

A value that specifies the type of sensor device represented by the object.


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
The <i>pType</i> parameter is null.

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
 




## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

