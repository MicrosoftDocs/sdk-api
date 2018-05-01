---
UID: NF:mfidl.IMFSensorGroup.GetSensorDeviceCount
title: IMFSensorGroup::GetSensorDeviceCount method
author: windows-driver-content
description: Gets the number of devices that are virtualized by the sensor group.
old-location: mf\imfsensorgroup_getsensordevicecount.htm
old-project: medfound
ms.assetid: 687A4275-5963-486E-8D59-B1858D7E388D
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetSensorDeviceCount method [Media Foundation], GetSensorDeviceCount method [Media Foundation], IMFSensorGroup interface, GetSensorDeviceCount,IMFSensorGroup.GetSensorDeviceCount, IMFSensorGroup, IMFSensorGroup interface [Media Foundation], GetSensorDeviceCount method, IMFSensorGroup::GetSensorDeviceCount, mf.imfsensorgroup_getsensordevicecount, mfidl/IMFSensorGroup::GetSensorDeviceCount
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
-	IMFSensorGroup.GetSensorDeviceCount
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorGroup::GetSensorDeviceCount method


## -description


Gets the number of devices that are virtualized by the sensor group.


## -parameters




### -param pdwCount [out]

The number of devices in the sensor group.


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

                The <i>pdwCount</i> parameter is null.

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




## -see-also




<a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>
 

 

