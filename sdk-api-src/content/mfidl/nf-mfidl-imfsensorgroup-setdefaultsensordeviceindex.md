---
UID: NF:mfidl.IMFSensorGroup.SetDefaultSensorDeviceIndex
title: IMFSensorGroup::SetDefaultSensorDeviceIndex
author: windows-driver-content
description: Configures one of the devices in the sensor group as the default device.
old-location: mf\imfsensorgroup_setdefaultsensordeviceindex.htm
old-project: medfound
ms.assetid: 06E2E2DB-8361-49BB-9369-0D0C33DF0C32
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFSensorGroup interface [Media Foundation],SetDefaultSensorDeviceIndex method, IMFSensorGroup.SetDefaultSensorDeviceIndex, IMFSensorGroup::SetDefaultSensorDeviceIndex, SetDefaultSensorDeviceIndex, SetDefaultSensorDeviceIndex method [Media Foundation], SetDefaultSensorDeviceIndex method [Media Foundation],IMFSensorGroup interface, mf.imfsensorgroup_setdefaultsensordeviceindex, mfidl/IMFSensorGroup::SetDefaultSensorDeviceIndex
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
-	IMFSensorGroup.SetDefaultSensorDeviceIndex
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorGroup::SetDefaultSensorDeviceIndex


## -description


Configures one of the devices in the sensor group as the default device.


## -parameters




### -param dwIndex

0-based index of the device to be set as defaut.  The index must be between 0 and the value returned by <a href="https://msdn.microsoft.com/687A4275-5963-486E-8D59-B1858D7E388D">GetSensorDeviceCount</a> - 1.


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
<dt><b>MF_E_INVALID_INDEX</b></dt>
</dl>
</td>
<td width="60%">

                the <i>dwIndex</i> parameter is not in the valid range.

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

If this method is not called, the first device in the Sensor Group (i.e. the device with index 0) will be used.




## -see-also




<a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>
 

 

