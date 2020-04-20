---
UID: NS:dxva9typ._DXVA_COPPSetProtectionLevelCmdData
title: DXVA_COPPSetProtectionLevelCmdData (dxva9typ.h)
description: Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).helpviewer_keywords: ["DXVA_COPPSetProtectionLevelCmdData","DXVA_COPPSetProtectionLevelCmdData structure [DirectShow]","DXVA_COPPSetProtectionLevelCmdDataStructure","_DXVA_COPPSetProtectionLevelCmdData","dshow.dxva_coppsetprotectionlevelcmddata","dxva9typ/DXVA_COPPSetProtectionLevelCmdData"]
old-location: dshow\dxva_coppsetprotectionlevelcmddata.htm
tech.root: DirectShow
ms.assetid: 19810f8f-2d23-4b01-864d-86ac82d40fe0
ms.date: 12/05/2018
ms.keywords: DXVA_COPPSetProtectionLevelCmdData, DXVA_COPPSetProtectionLevelCmdData structure [DirectShow], DXVA_COPPSetProtectionLevelCmdDataStructure, _DXVA_COPPSetProtectionLevelCmdData, dshow.dxva_coppsetprotectionlevelcmddata, dxva9typ/DXVA_COPPSetProtectionLevelCmdData
f1_keywords:
- dxva9typ/DXVA_COPPSetProtectionLevelCmdData
dev_langs:
- c++
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
targetos: Windows
req.typenames: DXVA_COPPSetProtectionLevelCmdData
req.redist: 
ms.custom: 19H1
---

# DXVA_COPPSetProtectionLevelCmdData structure


## -description



Contains data for the Set Protection Level command in Certified Output Protection Protocol (COPP).




## -struct-fields




### -field ProtType

Identifies the protection mechanism. See <a href="https://docs.microsoft.com/windows/desktop/DirectShow/copp-protection-type-flags">COPP Protection Type Flags</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level">COPP_ACP_Protection_Level</a>
</td>
</tr>
<tr>
<td>CGMS-A</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level">COPP_CGMSA_Protection_Level</a>
</td>
</tr>
<tr>
<td>HDCP</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level">COPP_HDCP_Protection_Level</a>
</td>
</tr>
</table>
 


### -field ExtendedInfoChangeMask

Reserved. Must be zero.


### -field ExtendedInfoData

Reserved. Must be zero.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
 

 

