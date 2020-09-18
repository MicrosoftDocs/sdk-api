---
UID: NF:iphlpapi.SetIpTTL
title: SetIpTTL function (iphlpapi.h)
description: The SetIpTTL function sets the default time-to-live (TTL) value for the local computer.
helpviewer_keywords: ["SetIpTTL","SetIpTTL function [IP Helper]","_iphlp_setipttl","iphlp.setipttl","iphlpapi/SetIpTTL"]
old-location: iphlp\setipttl.htm
tech.root: IpHlp
ms.assetid: dfde8712-f68f-4fa4-b939-ea36e23b5b1e
ms.date: 12/05/2018
ms.keywords: SetIpTTL, SetIpTTL function [IP Helper], _iphlp_setipttl, iphlp.setipttl, iphlpapi/SetIpTTL
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetIpTTL
 - iphlpapi/SetIpTTL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - SetIpTTL
---

# SetIpTTL function


## -description

The 
<b>SetIpTTL</b> function sets the default time-to-live (TTL) value for the local computer.

## -parameters

### -param nTTL [in]

The new TTL value for the local computer.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned on Windows Vista and Windows Server 2008 under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the  <i>nTTL</i> parameter is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The default TTL can also be set using the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatistics">SetIpStatistics</a> function.

On Windows Vista and later, the <b>SetIpTTL</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIpTTL</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatistics">SetIpStatistics</a> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>   On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipstats_lh">MIB_IPSTATS</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatistics">SetIpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipstatisticsex">SetIpStatisticsEx</a>