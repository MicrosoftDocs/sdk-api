---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTION0_
title: FWPM_CLASSIFY_OPTION0_
author: windows-sdk-content
description: The FWPM_CLASSIFY_OPTION0 structure.
old-location: fwp\fwpm_classify_option0.htm
old-project: FWP
ms.assetid: 11f2f873-d27e-411c-ba5b-a93134e1f027
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_CLASSIFY_OPTION0, FWPM_CLASSIFY_OPTION0 structure [Filtering], FWPM_CLASSIFY_OPTION0_, fwp.fwpm_classify_option0, fwpmtypes/FWPM_CLASSIFY_OPTION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_CLASSIFY_OPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_CLASSIFY_OPTION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

