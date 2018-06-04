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

# IPortableDeviceDispatchFactory::GetDeviceDispatch


## -description


Instantiates a WPD Automation <a href="wpdauto.device_object_script">Device</a> object for a given WPD device identifier.


## -parameters




### -param pszPnPDeviceID [in]

A pointer to a <b>String</b> that is used by Plug-and-play to identify a currently connected WPD device. The Plug and Play (PnP) identifier for a particular device can be obtained from the <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a> method in the WPD C++/COM API.


### -param ppDeviceDispatch [out]

Contains a pointer to the <b>IDispatch</b> implementation for the WPD Automation <a href="wpdauto.device_object_script">Device</a> object.



## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
</table>
 




## -remarks



 For an example of how to use <b>GetDeviceDispatch</b> method to instantiate a WPD Automation <b>Device</b>  object, see 
  <a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>.
      





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597563">Device Object</a>



<a href="https://msdn.microsoft.com/537551c9-0773-44a9-b602-7d2a6bf9ad00">IPortableDeviceDispatchFactory Interface</a>



<a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>
 

 

