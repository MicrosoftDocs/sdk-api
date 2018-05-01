---
UID: NF:mfidl.IMFSensorGroup.GetDefaultSensorDeviceIndex
title: IMFSensorGroup::GetDefaultSensorDeviceIndex method
author: windows-driver-content
description: Retrieves the index of the default device in the sensor group.
old-location: mf\imfsensorgroup_getdefaultsensordeviceindex.htm
old-project: medfound
ms.assetid: E82A83F7-E984-4353-8CED-E3B5EE28EB3D
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetDefaultSensorDeviceIndex method [Media Foundation], GetDefaultSensorDeviceIndex method [Media Foundation], IMFSensorGroup interface, GetDefaultSensorDeviceIndex,IMFSensorGroup.GetDefaultSensorDeviceIndex, IMFSensorGroup, IMFSensorGroup interface [Media Foundation], GetDefaultSensorDeviceIndex method, IMFSensorGroup::GetDefaultSensorDeviceIndex, mf.imfsensorgroup_getdefaultsensordeviceindex, mfidl/IMFSensorGroup::GetDefaultSensorDeviceIndex
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
req.typenames: MF_URL_TRUST_STATUS
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
-	IMFSensorGroup.GetDefaultSensorDeviceIndex
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorGroup::GetDefaultSensorDeviceIndex method


## -description


Retrieves the index of the default device in the sensor group.


## -parameters




### -param pdwIndex [out]

If the call succeeds, <i>pdwIndex</i> receives the index of the default device.


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

                The <i>pdwIndex</i> parameter is null.

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



The term "device" in this context could refer to a physical device, a custom media source, or a frame provider.

If this <a href="https://msdn.microsoft.com/06E2E2DB-8361-49BB-9369-0D0C33DF0C32">SetDefaultSensorDevice</a> has not been called, the first device in the Sensor Group (i.e. index 0) will be returned.




## -see-also




<a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>
 

 

