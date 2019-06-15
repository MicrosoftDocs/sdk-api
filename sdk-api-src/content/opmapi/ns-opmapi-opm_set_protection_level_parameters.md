---
UID: NS:opmapi._OPM_SET_PROTECTION_LEVEL_PARAMETERS
title: OPM_SET_PROTECTION_LEVEL_PARAMETERS (opmapi.h)
author: windows-sdk-content
description: Contains data for the OPM_SET_PROTECTION_LEVEL command in Output Protection Manager (OPM).
old-location: mf\opm_set_protection_level_parameters.htm
tech.root: medfound
ms.assetid: 074c30b2-ad79-4ace-89fb-859fac016ebf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OPM_SET_PROTECTION_LEVEL_PARAMETERS, OPM_SET_PROTECTION_LEVEL_PARAMETERS structure [Media Foundation], mf.opm_set_protection_level_parameters, opmapi/OPM_SET_PROTECTION_LEVEL_PARAMETERS
ms.topic: struct
f1_keywords: ["opmapi/OPM_SET_PROTECTION_LEVEL_PARAMETERS"]
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - opmapi.h
api_name:
 - OPM_SET_PROTECTION_LEVEL_PARAMETERS
product: Windows
targetos: Windows
req.typenames: OPM_SET_PROTECTION_LEVEL_PARAMETERS
req.redist: 
ms.custom: 19H1
---

# OPM_SET_PROTECTION_LEVEL_PARAMETERS structure


## -description


Contains data for the <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-set-protection-level">OPM_SET_PROTECTION_LEVEL</a> command in <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM).


## -struct-fields




### -field ulProtectionType

Identifies the protection mechanism. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/medfound/opm-protection-type-flags">OPM Protection Type Flags</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/ne-opmapi-_opm_acp_protection_level">OPM_ACP_PROTECTION_LEVEL</a>
</td>
</tr>
<tr>
<td>CGMS-A</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/cgms-a-protection-flags">CGMS-A Protection Flags</a>
</td>
</tr>
<tr>
<td>DPCP</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/ne-opmapi-_opm_dpcp_protection_level">OPM_DPCP_PROTECTION_LEVEL</a>
</td>
</tr>
<tr>
<td>HDCP</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/ne-opmapi-_opm_hdcp_protection_level">OPM_HDCP_PROTECTION_LEVEL</a>
</td>
</tr>
</table>
 


### -field Reserved

Reserved for future use. Set to zero.


### -field Reserved2

Reserved for future use. Set to zero.


## -remarks



The layout of this structure is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/dxva9typ/ns-dxva9typ-_dxva_coppsetprotectionlevelcmddata">DXVA_COPPSetProtectionLevelCmdData</a> structure used in Certified Output Protection Protocol (COPP).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 

