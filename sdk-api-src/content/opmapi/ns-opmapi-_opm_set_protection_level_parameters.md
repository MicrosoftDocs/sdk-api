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

# _OPM_SET_PROTECTION_LEVEL_PARAMETERS structure


## -description


Contains data for the <a href="https://msdn.microsoft.com/f4e63bf5-0749-4054-9f86-7fd88f2881ad">OPM_SET_PROTECTION_LEVEL</a> command in <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM).


## -struct-fields




### -field ulProtectionType

Identifies the protection mechanism. For a list of possible values, see <a href="https://msdn.microsoft.com/484dfea9-301d-4b2b-b5d1-d785ebaa8c8f">OPM Protection Type Flags</a>.


### -field ulProtectionLevel

Specifies the protection level. The meaning of this value depends on the protection mechanism that is queried. For each protection mechanism, the value is a flag from a different enumeration, as shown in the following table.



<table>
<tr>
<th>Protection mechanism</th>
<th>Enumeration</th>
</tr>
<tr>
<td>ACP</td>
<td>
<a href="https://msdn.microsoft.com/f52b4ee6-1ab3-4153-86e3-5ae69fd8a958">OPM_ACP_PROTECTION_LEVEL</a>
</td>
</tr>
<tr>
<td>CGMS-A</td>
<td>
<a href="https://msdn.microsoft.com/739e2f9e-b8f1-4ee1-8706-9a069773a3de">CGMS-A Protection Flags</a>
</td>
</tr>
<tr>
<td>DPCP</td>
<td>
<a href="https://msdn.microsoft.com/c761f3c1-f18e-4ae9-9aa1-1ba440a6c8df">OPM_DPCP_PROTECTION_LEVEL</a>
</td>
</tr>
<tr>
<td>HDCP</td>
<td>
<a href="https://msdn.microsoft.com/698050e4-9726-49fa-85ed-9ae057e8c308">OPM_HDCP_PROTECTION_LEVEL</a>
</td>
</tr>
</table>
 


### -field Reserved

Reserved for future use. Set to zero.


### -field Reserved2

Reserved for future use. Set to zero.


## -remarks



The layout of this structure is identical to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563143">DXVA_COPPSetProtectionLevelCmdData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

