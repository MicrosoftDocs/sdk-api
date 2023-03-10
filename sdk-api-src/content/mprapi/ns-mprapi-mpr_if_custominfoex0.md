---
UID: NS:mprapi._MPR_IF_CUSTOMINFOEX0
title: MPR_IF_CUSTOMINFOEX0 (mprapi.h)
description: Gets or sets tunnel specific custom configuration for a demand dial interfaces.
helpviewer_keywords: ["*PMPR_IF_CUSTOMINFOEX0","MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2","MPR_IF_CUSTOMINFOEX0","MPR_IF_CUSTOMINFOEX0 structure [RAS]","PMPR_IF_CUSTOMINFOEX0","PMPR_IF_CUSTOMINFOEX0 structure pointer [RAS]","mprapi/MPR_IF_CUSTOMINFOEX0","mprapi/PMPR_IF_CUSTOMINFOEX0","rras.mpr_if_custominfoex0"]
old-location: rras\mpr_if_custominfoex0.htm
tech.root: RRAS
ms.assetid: 53c4b7ae-db73-4d97-a99f-a98354c48a92
ms.date: 12/05/2018
ms.keywords: '*PMPR_IF_CUSTOMINFOEX0, MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2, MPR_IF_CUSTOMINFOEX0, MPR_IF_CUSTOMINFOEX0 structure [RAS], PMPR_IF_CUSTOMINFOEX0, PMPR_IF_CUSTOMINFOEX0 structure pointer [RAS], mprapi/MPR_IF_CUSTOMINFOEX0, mprapi/PMPR_IF_CUSTOMINFOEX0, rras.mpr_if_custominfoex0'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: MPR_IF_CUSTOMINFOEX0, *PMPR_IF_CUSTOMINFOEX0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_IF_CUSTOMINFOEX0
 - mprapi/_MPR_IF_CUSTOMINFOEX0
 - PMPR_IF_CUSTOMINFOEX0
 - mprapi/PMPR_IF_CUSTOMINFOEX0
 - MPR_IF_CUSTOMINFOEX0
 - mprapi/MPR_IF_CUSTOMINFOEX0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mprapi.h
api_name:
 - MPR_IF_CUSTOMINFOEX0
---

# MPR_IF_CUSTOMINFOEX0 structure


## -description

Gets or sets tunnel specific custom configuration for a demand dial interfaces.

Do not use the <b>MPR_IF_CUSTOMINFOEX0</b> structure directly in your code; using <a href="/windows/desktop/RRAS/router-management-data-types">MPR_IF_CUSTOMINFOEX</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>MPR_IF_CUSTOMINFOEX0</b> structure.

### -field dwFlags

A value that specifies the tunnel type for which the custom configuration is available. The following values are supported.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
No custom configuration available.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2_"></a><a id="mprapi_if_custom_config_for_ikev2_"></a><dl>
<dt><b>MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2 </b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
IKEv2 tunnel specific configuration is available.

</td>
</tr>
</table>

### -field customIkev2Config

A <a href="/windows/desktop/api/mprapi/ns-mprapi-router_ikev2_if_custom_config0">ROUTER_IKEv2_IF_CUSTOM_CONFIG0</a> structure that specifies the IKEv2 tunnel configuration parameters.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetcustominfoex">MprAdminInterfaceGetCustomInfoEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetcustominfoex">MprAdminInterfaceSetCustomInfoEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacegetcustominfoex">MprConfigInterfaceGetCustomInfoEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacesetcustominfoex">MprConfigInterfaceSetCustomInfoEx</a>