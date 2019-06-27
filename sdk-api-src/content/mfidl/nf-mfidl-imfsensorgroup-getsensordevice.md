---
UID: NF:mfidl.IMFSensorGroup.GetSensorDevice
title: IMFSensorGroup::GetSensorDevice (mfidl.h)
author: windows-sdk-content
description: Gets the IMFSensorDevice corresponding to a device in the sensor group.
old-location: mf\imfsensorgroup_getsensordevice.htm
tech.root: medfound
ms.assetid: 78924C45-9612-4B39-B9E2-C8D2DCCBED79
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSensorDevice, GetSensorDevice method [Media Foundation], GetSensorDevice method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetSensorDevice method, IMFSensorGroup.GetSensorDevice, IMFSensorGroup::GetSensorDevice, mf.imfsensorgroup_getsensordevice, mfidl/IMFSensorGroup::GetSensorDevice
ms.topic: method
f1_keywords: 
 - "mfidl/IMFSensorGroup.GetSensorDevice"
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
 - IMFSensorGroup.GetSensorDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorGroup::GetSensorDevice


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a> corresponding to a device in the sensor group.


## -parameters




### -param dwIndex [in]

The 0-based index of the device to be retrieved.  The index must be between 0 and the value returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-getsensordevicecount">GetSensorDeviceCount</a> - 1.


### -param ppDevice [out]

If the call is successful, <i>ppDevice</i> will contain the retrieved sensor device.


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
The <i>ppDevice</i> parameter is null.

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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>
 

 

