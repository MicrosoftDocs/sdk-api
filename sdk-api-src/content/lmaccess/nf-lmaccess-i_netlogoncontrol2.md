---
UID: NF:lmaccess.I_NetLogonControl2
title: I_NetLogonControl2 function (lmaccess.h)
description: Controls various aspects of the Netlogon service.
helpviewer_keywords: ["I_NetLogonControl2","I_NetLogonControl2 function [Windows API]","NETLOGON_CONTROL_CHANGE_PASSWORD","NETLOGON_CONTROL_FORCE_DNS_REG","NETLOGON_CONTROL_PDC_REPLICATE","NETLOGON_CONTROL_QUERY","NETLOGON_CONTROL_QUERY_DNS_REG","NETLOGON_CONTROL_REDISCOVER","NETLOGON_CONTROL_REPLICATE","NETLOGON_CONTROL_SYNCHRONIZE","NETLOGON_CONTROL_TC_QUERY","NETLOGON_CONTROL_TC_VERIFY","NETLOGON_INFO_1","NETLOGON_INFO_2","NETLOGON_INFO_3","NETLOGON_INFO_4","lmaccess/I_NetLogonControl2","winprog.i_netlogoncontrol2"]
old-location: winprog\i_netlogoncontrol2.htm
tech.root: winprog
ms.assetid: bf40ee60-3a13-4a4e-a0f4-ba7c9fc11097
ms.date: 12/05/2018
ms.keywords: I_NetLogonControl2, I_NetLogonControl2 function [Windows API], NETLOGON_CONTROL_CHANGE_PASSWORD, NETLOGON_CONTROL_FORCE_DNS_REG, NETLOGON_CONTROL_PDC_REPLICATE, NETLOGON_CONTROL_QUERY, NETLOGON_CONTROL_QUERY_DNS_REG, NETLOGON_CONTROL_REDISCOVER, NETLOGON_CONTROL_REPLICATE, NETLOGON_CONTROL_SYNCHRONIZE, NETLOGON_CONTROL_TC_QUERY, NETLOGON_CONTROL_TC_VERIFY, NETLOGON_INFO_1, NETLOGON_INFO_2, NETLOGON_INFO_3, NETLOGON_INFO_4, lmaccess/I_NetLogonControl2, winprog.i_netlogoncontrol2
req.header: lmaccess.h
req.include-header: 
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - I_NetLogonControl2
 - lmaccess/I_NetLogonControl2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - I_NetLogonControl2
---

# I_NetLogonControl2 function


## -description

The <b>I_NetLogonControl2</b> function controls various aspects of the Netlogon service.

## -parameters

### -param ServerName [in, optional]

The name of the remote server.

### -param FunctionCode [in]

The operation to be performed. This value  can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_QUERY"></a><a id="netlogon_control_query"></a><dl>
<dt><b>NETLOGON_CONTROL_QUERY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
No operation. Returns only the requested information.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_REPLICATE"></a><a id="netlogon_control_replicate"></a><dl>
<dt><b>NETLOGON_CONTROL_REPLICATE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Forces the security account manager (SAM) database on a backup domain controller (BDC) to be brought in sync with the copy on the primary domain controller (PDC). This operation does not imply a full synchronize. The Netlogon service replicates any outstanding differences if possible.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_SYNCHRONIZE"></a><a id="netlogon_control_synchronize"></a><dl>
<dt><b>NETLOGON_CONTROL_SYNCHRONIZE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Forces a BDC to get a new copy of the SAM database from the PDC. This operation performs a full synchronize.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_PDC_REPLICATE"></a><a id="netlogon_control_pdc_replicate"></a><dl>
<dt><b>NETLOGON_CONTROL_PDC_REPLICATE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Forces a PDC to ask for each BDC to replicate now.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_REDISCOVER"></a><a id="netlogon_control_rediscover"></a><dl>
<dt><b>NETLOGON_CONTROL_REDISCOVER</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Forces a domain controller (DC) to rediscover the specified trusted domain DC.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_TC_QUERY"></a><a id="netlogon_control_tc_query"></a><dl>
<dt><b>NETLOGON_CONTROL_TC_QUERY</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Queries  the secure channel, requesting a status update about its last usage.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_TC_VERIFY"></a><a id="netlogon_control_tc_verify"></a><dl>
<dt><b>NETLOGON_CONTROL_TC_VERIFY</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Verifies the current status of the specified trusted domain secure channel. If the status indicates success, the domain controller is pinged. If the status or the ping indicates failure, a new trusted domain controller is rediscovered.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_CHANGE_PASSWORD"></a><a id="netlogon_control_change_password"></a><dl>
<dt><b>NETLOGON_CONTROL_CHANGE_PASSWORD</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Forces a password change on a secure channel to a trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_FORCE_DNS_REG"></a><a id="netlogon_control_force_dns_reg"></a><dl>
<dt><b>NETLOGON_CONTROL_FORCE_DNS_REG</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Forces the domain controller to re-register all of its DNS records. The <i>QueryLevel</i> parameter must be set to 1.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_CONTROL_QUERY_DNS_REG"></a><a id="netlogon_control_query_dns_reg"></a><dl>
<dt><b>NETLOGON_CONTROL_QUERY_DNS_REG</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Issues a query requesting the status of DNS updates performed by the Netlogon service. If any DNS registration or deregistration errors occurred on the last update, the result is negative. The <i>QueryLevel</i> parameter must be set to 1.

</td>
</tr>
</table>

### -param QueryLevel [in]

Indicates what information should be returned from the Netlogon service. This value can be any of the following structures.



#### NETLOGON_INFO_1 (1)



#### NETLOGON_INFO_2 (2)



#### NETLOGON_INFO_3 (3)



#### NETLOGON_INFO_4 (4)

### -param Data [in]

Carries input data that depends on the value specified in the <i>FunctionCode</i> parameter. The NETLOGON_CONTROL_REDISCOVER and NETLOGON_CONTROL_TC_QUERY function codes specify the trusted domain name (the data type is <b>LPWSTR *</b>).

### -param Buffer [out]

Returns a pointer to a buffer that contains the requested information in the structure passed in the <i>QueryLevel</i> parameter.

 The buffer must be freed using <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.

## -returns

The method returns 0x00000000 (<b>NERR_Success</b>) on success; otherwise, it returns a nonzero error code defined in Lmerr.h or Winerror.h. NET_API_STATUS error codes begin with the value 0x00000834. For more information about network management error codes, see <a href="/windows/desktop/NetMgmt/network-management-error-codes">Network_Management_Error_Codes</a>. The following table describes possible return values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_Success</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The method call completed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Access validation on the caller returns false. Access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>0x00000032</dt>
</dl>
</td>
<td width="60%">
A function code is not valid on the specified
        server.  For example,  NETLOGON_CONTROL_REPLICATE might have been passed to a primary domain controller (PDC).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>0x00000057</dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
<dt>0x0000007C</dt>
</dl>
</td>
<td width="60%">
The query call level is not correct.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
<dt>0x000004261210121</dt>
</dl>
</td>
<td width="60%">
The service has not been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_INVALID_COMPUTERNAME</b></dt>
<dt> 0x000004BA</dt>
</dl>
</td>
<td width="60%">
The format of the specified computer name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_LOGON_SERVERS</b></dt>
<dt>0x0000051F</dt>
</dl>
</td>
<td width="60%">
There are currently no logon servers available to service the logon request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DOMAIN_ROLE</b></dt>
<dt>0x0000054A</dt>
</dl>
</td>
<td width="60%">
Password change for an interdomain trust account was attempted  on a backup domain controller (BDC). This operation is only allowed for the PDC of the domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
<dt>0x0000054B</dt>
</dl>
</td>
<td width="60%">
The specified domain either does not exist or could not be contacted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserNotFound</b></dt>
<dt>0x000008AD</dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

</td>
</tr>
</table>

## -remarks

This function can be used to request that a BDC ensure that its copy of the SAM database is brought up-to-date. It can also be used to determine if a BDC currently has a secure channel open to the PDC.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-netlogon_info_1">NETLOGON_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-netlogon_info_2">NETLOGON_INFO_2</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-netlogon_info_3">NETLOGON_INFO_3</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-netlogon_info_4">NETLOGON_INFO_4</a>