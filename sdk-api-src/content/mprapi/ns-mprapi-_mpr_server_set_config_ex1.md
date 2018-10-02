---
UID: NS:mprapi._MPR_SERVER_SET_CONFIG_EX1
title: "_MPR_SERVER_SET_CONFIG_EX1"
author: windows-sdk-content
description: Used to get or set the tunnel configuration information of a RAS server.
old-location: rras\mpr_server_set_config_ex.htm
tech.root: RRAS
ms.assetid: 6c993c9c-4522-4758-926a-fa7ef2a89418
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMPR_SERVER_SET_CONFIG_EX1, MPRAPI_SET_CONFIG_PROTOCOL_FOR_IKEV2, MPRAPI_SET_CONFIG_PROTOCOL_FOR_L2TP, MPRAPI_SET_CONFIG_PROTOCOL_FOR_PPTP, MPRAPI_SET_CONFIG_PROTOCOL_FOR_SSTP, MPR_SERVER_SET_CONFIG_EX, MPR_SERVER_SET_CONFIG_EX structure [RAS], MPR_SERVER_SET_CONFIG_EX1, PMPR_SERVER_SET_CONFIG_EX, PMPR_SERVER_SET_CONFIG_EX structure pointer [RAS], _MPR_SERVER_SET_CONFIG_EX0, _MPR_SERVER_SET_CONFIG_EX1, mprapi/MPR_SERVER_SET_CONFIG_EX, mprapi/PMPR_SERVER_SET_CONFIG_EX, rras.mpr_server_set_config_ex"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Mprapi.h
api_name:
 - MPR_SERVER_SET_CONFIG_EX
product: Windows
targetos: Windows
req.typenames: MPR_SERVER_SET_CONFIG_EX1, *PMPR_SERVER_SET_CONFIG_EX1
req.redist: 
---

# _MPR_SERVER_SET_CONFIG_EX1 structure


## -description


The <b>MPR_SERVER_SET_CONFIG_EX</b> structure is used to get or set the tunnel configuration information of a RAS server.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/2f4e1ddc-7991-4091-9889-fdd2d75e702f">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>MPR_SERVER_SET_CONFIG_EX</b> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>MPRAPI_MPR_SERVER_SET_CONFIG_OBJECT_REVISION_1</b> and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT</b>.</div>
<div> </div>

### -field setConfigForProtocols

A value that specifies the tunnel type in <b>ConfigParams</b>. The following tunnel types are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_SET_CONFIG_PROTOCOL_FOR_PPTP_________________"></a><a id="mprapi_set_config_protocol_for_pptp_________________"></a><dl>
<dt><b>MPRAPI_SET_CONFIG_PROTOCOL_FOR_PPTP                 </b></dt>
</dl>
</td>
<td width="60%">
Point-to-Point Protocol (PPTP)

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_SET_CONFIG_PROTOCOL_FOR_L2TP_________________"></a><a id="mprapi_set_config_protocol_for_l2tp_________________"></a><dl>
<dt><b>MPRAPI_SET_CONFIG_PROTOCOL_FOR_L2TP                 </b></dt>
</dl>
</td>
<td width="60%">
Layer 2 Tunneling Protocol (L2TP)

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_SET_CONFIG_PROTOCOL_FOR_SSTP_________________"></a><a id="mprapi_set_config_protocol_for_sstp_________________"></a><dl>
<dt><b>MPRAPI_SET_CONFIG_PROTOCOL_FOR_SSTP                 </b></dt>
</dl>
</td>
<td width="60%">
Secure Socket Tunneling Protocol (SSTP)

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_SET_CONFIG_PROTOCOL_FOR_IKEV2_________________"></a><a id="mprapi_set_config_protocol_for_ikev2_________________"></a><dl>
<dt><b>MPRAPI_SET_CONFIG_PROTOCOL_FOR_IKEV2                 </b></dt>
</dl>
</td>
<td width="60%">
Internet Key version 2 (IKEV2)

</td>
</tr>
</table>
 


### -field ConfigParams

A <a href="https://msdn.microsoft.com/19ad3493-99b7-405f-9663-3886388b5640">MPRAPI_TUNNEL_CONFIG_PARAMS</a> structure that contains the tunnel configuration information for the tunnel type specified in <b>setConfigForProtocols</b>.


## -see-also




<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

