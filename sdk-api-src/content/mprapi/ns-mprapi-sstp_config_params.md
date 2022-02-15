---
UID: NS:mprapi._SSTP_CONFIG_PARAMS
title: SSTP_CONFIG_PARAMS (mprapi.h)
description: Used to get and set the device configuration for Secure Socket Tunneling Protocol (SSTP) on a RAS Server.
helpviewer_keywords: ["*PSSTP_CONFIG_PARAMS","CALG_SHA_256","MPR_ENABLE_RAS_ON_DEVICE","SSTP_CONFIG_PARAMS","SSTP_CONFIG_PARAMS structure [RAS]","mprapi/SSTP_CONFIG_PARAMS","rras.sstp_config_params"]
old-location: rras\sstp_config_params.htm
tech.root: RRAS
ms.assetid: 6f21d569-af9b-49ba-ab02-4dfc74e87ed2
ms.date: 12/05/2018
ms.keywords: '*PSSTP_CONFIG_PARAMS, CALG_SHA_256, MPR_ENABLE_RAS_ON_DEVICE, SSTP_CONFIG_PARAMS, SSTP_CONFIG_PARAMS structure [RAS], mprapi/SSTP_CONFIG_PARAMS, rras.sstp_config_params'
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
targetos: Windows
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SSTP_CONFIG_PARAMS
 - mprapi/_SSTP_CONFIG_PARAMS
 - PSSTP_CONFIG_PARAMS
 - mprapi/PSSTP_CONFIG_PARAMS
 - SSTP_CONFIG_PARAMS
 - mprapi/SSTP_CONFIG_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - SSTP_CONFIG_PARAMS
---

# SSTP_CONFIG_PARAMS structure


## -description

The <b>SSTP_CONFIG_PARAMS</b> structure is used to get and set the device configuration for Secure Socket Tunneling Protocol (SSTP) on a RAS Server.

## -struct-fields

### -field dwNumPorts

A value that specifies the number of ports configured on the RRAS server to accept SSTP connections. The maximum values for <b>dwNumPorts</b> are listed in the following table. The value zero is not allowed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows Web Server 2008

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Standard

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 Datacenter and Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If <b>dwNumPorts</b> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfoex">MprConfigServerGetInfoEx</a> and <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfoex">MprConfigServerSetInfoEx</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.</div>
<div> </div>

### -field dwPortFlags

A value that specifies the type of ports configured on the  RRAS server for SSTP. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_ENABLE_RAS_ON_DEVICE"></a><a id="mpr_enable_ras_on_device"></a><dl>
<dt><b>MPR_ENABLE_RAS_ON_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
If set, RAS is enabled on the device.

</td>
</tr>
</table>

### -field isUseHttps

A value that is <b>TRUE</b> if HTTPS is used and <b>FALSE</b> otherwise.

### -field certAlgorithm

A value that specifies the certificate hashing algorithm used. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_SHA_256"></a><a id="calg_sha_256"></a><dl>
<dt><b>CALG_SHA_256</b></dt>
</dl>
</td>
<td width="60%">
256-bit SHA hashing algorithm

</td>
</tr>
</table>

### -field sstpCertDetails

An <a href="/windows/desktop/api/mprapi/ns-mprapi-sstp_cert_info">SSTP_CERT_INFO</a> structure that contains the SSTP based certificate hash.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_tunnel_config_params0">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>