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

# _DXVA_COPPSetProtectionLevelCmdData structure


## -description



Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).




## -struct-fields




### -field ProtType

Identifies the protection mechanism. See <a href="https://msdn.microsoft.com/a3cd63d8-22a5-473c-83c2-3499f3d32671">COPP Protection Type Flags</a>.


### -field ProtLevel

Specifies the protection level. The meaning of this value depends on the protection mechanism that is queried. For each protection mechanism, the value of the <code>ProtLevel</code> member is a flag from a different enumeration, as shown in the following table.

<table>
<tr>
<th>Protection mechanism</th>
<th>Enumeration</th>
</tr>
<tr>
<td>ACP</td>
<td>
<a href="https://msdn.microsoft.com/a3149eb6-e758-4b21-b574-32fb6c2ae3a2">COPP_ACP_Protection_Level</a>
</td>
</tr>
<tr>
<td>CGMS-A</td>
<td>
<a href="https://msdn.microsoft.com/37b453fa-c976-4b13-b94a-1eebd8ecd44b">COPP_CGMSA_Protection_Level</a>
</td>
</tr>
<tr>
<td>HDCP</td>
<td>
<a href="https://msdn.microsoft.com/902ea4c6-8eba-4bfd-b986-5e7a5a2a5971">COPP_HDCP_Protection_Level</a>
</td>
</tr>
</table>
 


### -field ExtendedInfoChangeMask

Reserved. Must be zero.


### -field ExtendedInfoData

Reserved. Must be zero.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

