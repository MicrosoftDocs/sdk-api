---
UID: NS:dxva9typ._DXVA_COPPSetProtectionLevelCmdData
title: DXVA_COPPSetProtectionLevelCmdData (dxva9typ.h)
author: windows-sdk-content
description: Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).
old-location: dshow\dxva_coppsetprotectionlevelcmddata.htm
tech.root: DirectShow
ms.assetid: 19810f8f-2d23-4b01-864d-86ac82d40fe0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVA_COPPSetProtectionLevelCmdData, DXVA_COPPSetProtectionLevelCmdData structure [DirectShow], DXVA_COPPSetProtectionLevelCmdDataStructure, _DXVA_COPPSetProtectionLevelCmdData, dshow.dxva_coppsetprotectionlevelcmddata, dxva9typ/DXVA_COPPSetProtectionLevelCmdData
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVA_COPPSetProtectionLevelCmdData
product: Windows
targetos: Windows
req.typenames: DXVA_COPPSetProtectionLevelCmdData
req.redist: 
---

# DXVA_COPPSetProtectionLevelCmdData structure


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
 

 

