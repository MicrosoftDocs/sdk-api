---
UID: NF:mfidl.IMFSensorGroup.GetFlags
title: IMFSensorGroup::GetFlags
author: windows-sdk-content
description: Gets the flags set for the sensor group.
old-location: mf\imfsensorgroup_getflags.htm
tech.root: medfound
ms.assetid: 99143CFD-930A-405C-A8FB-8DBF52CD9BB5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetFlags method, IMFSensorGroup.GetFlags, IMFSensorGroup::GetFlags, mf.imfsensorgroup_getflags, mfidl/IMFSensorGroup::GetFlags
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
 - IMFSensorGroup.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorGroup::GetFlags


## -description


Gets the flags set for the sensor group.


## -parameters




### -param pFlags [out]

The flags set for the sensor group


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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor group has not been initialized.

</td>
</tr>
</table>
 




## -remarks



Currently, no flags are defined for Sensor Groups.




## -see-also




<a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a>
 

 

