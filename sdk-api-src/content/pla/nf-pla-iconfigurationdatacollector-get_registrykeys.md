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

# IConfigurationDataCollector::get_RegistryKeys


## -description


Retrieves or sets a list of registry keys to collect.

This property is read/write.


## -parameters


## -remarks



You can collect registry data from the following registry hives:

<ul>
<li><b>HKEY_CLASSES_ROOT</b></li>
<li><b>HKEY_CURRENT_CONFIG</b></li>
<li><b>HKEY_CURRENT_USER</b></li>
<li><b>HKEY_LOCAL_MACHINE</b></li>
<li><b>HKEY_USERS</b></li>
</ul>
To collect a registry value, specify the full path to the value name, for example, <b>\HKEY_LOCAL_MACHINE\MyKey\MyValue</b>.

To collect all the values under a registry key, specify the full path to the registry key, for example, <b>\HKEY_LOCAL_MACHINE\MyKey\</b>.

To collect all the values under a registry key and its subkeys, use two backslashes for the last path delimiter, for example, <b>\\computername\HKEY_LOCAL_MACHINE\MyKey\\</b>. PLA recursively collects the registry data down to the level specified in the <a href="https://msdn.microsoft.com/f291a404-a952-42cd-a538-c7d326aa29d8">IConfigurationDataCollector::RegistryMaxRecursiveDepth</a> property.

To collect registry information from a remote computer, include the computer name at the beginning of the registry path, for example, <b>\\computername\HKEY_LOCAL_MACHINE\MyKey\MyValue</b>.




## -see-also




<a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a>



<a href="https://msdn.microsoft.com/f291a404-a952-42cd-a538-c7d326aa29d8">IConfigurationDataCollector::RegistryMaxRecursiveDepth</a>
 

 

