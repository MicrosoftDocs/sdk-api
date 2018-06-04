---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMDeviceManager2::GetDeviceFromCanonicalName


## -description


The <b>GetDeviceFromCanonicalName</b> method retrieves an <b>IWMDMDevice</b> interface for a device with a specified canonical name. You can retrieve a device's canonical name by calling <a href="https://msdn.microsoft.com/16e18a9e-315f-41a2-b895-e3e478720864">IWMDMDevice2::GetCanonicalName</a>.


## -parameters




### -param pwszCanonicalName

A wide-character, <b>null</b>-terminated string specifying the canonical name of the device.


### -param ppDevice






#### - ppDeviceArray

Pointer to a pointer to the <a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice</a> interface of the device object with the specified canonical name. The caller must release this interface when done with it.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszCanonicalName</i> or <i>ppDeviceArray</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no connected device found with canonical name <i>pwszCanonicalName</i>.

</td>
</tr>
</table>
 




## -remarks



This method can be useful if an application implements <a href="https://msdn.microsoft.com/3089a04d-24f5-4a4c-9df5-b4073fef358a">IWMDMNotification</a>, which sends a canonical name notification when a device connects or disconnects from the computer.




## -see-also




<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/ea4bf623-c93a-4c0f-a84f-e3a979b37d60">IWMDeviceManager2 Interface</a>
 

 

