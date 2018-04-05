---
UID: NS:mprapi._SSTP_CONFIG_PARAMS
title: "_SSTP_CONFIG_PARAMS"
author: windows-driver-content
description: Used to get and set the device configuration for Secure Socket Tunneling Protocool (SSTP) on a RAS Server.
old-location: rras\sstp_config_params.htm
old-project: RRAS
ms.assetid: 6f21d569-af9b-49ba-ab02-4dfc74e87ed2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PSSTP_CONFIG_PARAMS, CALG_SHA_256, MPR_ENABLE_RAS_ON_DEVICE, SSTP_CONFIG_PARAMS, SSTP_CONFIG_PARAMS structure [RAS], _SSTP_CONFIG_PARAMS, mprapi/SSTP_CONFIG_PARAMS, rras.sstp_config_params"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	SSTP_CONFIG_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SSTP_CONFIG_PARAMS structure


## -description


The <b>SSTP_CONFIG_PARAMS</b> structure is used to get and set the device configuration for Secure Socket Tunneling Protocool (SSTP) on a RAS Server.


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
Windows Server 2008 Datacenterand Windows Server 2008 Enterprise

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If <b>dwNumPorts</b> contains a value beyond the limit configured in the registry at service start time (the default is 1000 for Windows Server 2008 Standard and Windows Server 2008 Enterprise), the <a href="https://msdn.microsoft.com/654d1410-b54c-4284-bf7f-f6ae6b7ef85e">MprConfigServerGetInfoEx</a> and <a href="https://msdn.microsoft.com/8251f391-7697-4024-9a9d-c7c810129a78">MprConfigServerSetInfoEx</a> functions will return <b>ERROR_SUCCESS_REBOOT_REQUIRED</b>.</div>
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

An <a href="https://msdn.microsoft.com/004fce6d-c617-4356-9a8f-f7b4fbb3d4c2">SSTP_CERT_INFO</a> structure that contains the SSTP based certificate hash.


## -see-also




<a href="https://msdn.microsoft.com/19ad3493-99b7-405f-9663-3886388b5640">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

