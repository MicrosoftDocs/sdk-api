---
UID: NF:mfidl.IMFSensorDevice.GetSensorDeviceMode
title: IMFSensorDevice::GetSensorDeviceMode
author: windows-sdk-content
description: Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.
old-location: mf\imfsensordevice_getsensordevicemode.htm
old-project: medfound
ms.assetid: 21594884-DAA5-450C-855D-E800FE164C5E
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetSensorDeviceMode, GetSensorDeviceMode method [Media Foundation], GetSensorDeviceMode method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetSensorDeviceMode method, IMFSensorDevice.GetSensorDeviceMode, IMFSensorDevice::GetSensorDeviceMode, mf.imfsensordevice_getsensordevicemode, mfidl/IMFSensorDevice::GetSensorDeviceMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
 - IMFSensorDevice.GetSensorDeviceMode
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorDevice::GetSensorDeviceMode


## -description


Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.


## -parameters




### -param peMode

If the call succeeds, receives a member of the <a href="https://msdn.microsoft.com/D405AB48-13EC-4859-91B6-0DB797F85DBE">MFSensorDeviceMode</a>, specifying the current mode of the sendsor device.


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
 




## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

