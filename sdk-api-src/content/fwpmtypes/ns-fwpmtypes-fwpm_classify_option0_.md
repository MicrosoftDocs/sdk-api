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

# FWPM_CLASSIFY_OPTION0_ structure


## -description


The <b>FWPM_CLASSIFY_OPTION0</b> structure is used to define unicast and multicast timeout options and data.


## -struct-fields




### -field type

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552428">FWP_CLASSIFY_OPTION_TYPE</a> value.


### -field value

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> structure.


## -remarks



The following table lists possible values for the members of a <b>FWPM_CLASSIFY_OPTION0</b> structure.

<table>
<tr>
<th><b>type</b></th>
<th><b>value</b></th>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_MULTICAST_STATE</td>
<td>
<ul>
<li>FWP_OPTION_VALUE_ALLOW_MULTICAST_STATE Allow link-local multicast state creation on outbound traffic

</li>
<li>FWP_OPTION_VALUE_DENY_MULTICAST_STATE  Do not allow link-local multicast state creation on outbound traffic

</li>
<li>FWP_OPTION_VALUE_ALLOW_GLOBAL_MULTICAST_STATE Allow global multicast state creation on outbound traffic

</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING</td>
<td>
<ul>
<li>FWP_OPTION_VALUE_ENABLE_LOOSE_SOURCE Enable loose source mapping

</li>
<li>FWP_OPTION_VALUE_DISABLE_LOOSE_SOURCE Disable loose source mapping

</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_UNICAST_LIFETIME</td>
<td>
<ul>
<li>Any FWP_UINT32</li>
</ul>
</td>
</tr>
<tr>
<td>FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME</td>
<td>
<ul>
<li>Any FWP_UINT32</li>
</ul>
</td>
</tr>
</table>
 

<b>FWPM_CLASSIFY_OPTION0</b> is a specific implementation of FWPM_CLASSIFY_OPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550079">FWPM_CLASSIFY_OPTIONS0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552428">FWP_CLASSIFY_OPTION_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

