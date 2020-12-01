---
UID: NF:iphlpapi.FlushIpNetTable
title: FlushIpNetTable function (iphlpapi.h)
description: The FlushIpNetTable function deletes all ARP entries for the specified interface from the ARP table on the local computer.
helpviewer_keywords: ["FlushIpNetTable","FlushIpNetTable function [IP Helper]","_iphlp_flushipnettable","iphlp.flushipnettable","iphlpapi/FlushIpNetTable"]
old-location: iphlp\flushipnettable.htm
tech.root: IpHlp
ms.assetid: cf4dea10-552d-4730-a452-9302ef3761ff
ms.date: 12/05/2018
ms.keywords: FlushIpNetTable, FlushIpNetTable function [IP Helper], _iphlp_flushipnettable, iphlp.flushipnettable, iphlpapi/FlushIpNetTable
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
 - FlushIpNetTable
 - iphlpapi/FlushIpNetTable
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
 - FlushIpNetTable
---

# FlushIpNetTable function


## -description

The 
<b>FlushIpNetTable</b> function deletes all ARP entries for the specified interface from the ARP table on the local computer.

## -parameters

### -param dwIfIndex [in]

The index of the interface for which to delete all ARP entries.

## -returns

The function returns <b>NO_ERROR</b> (zero) if the function is successful. 

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
An input parameter is invalid, no action was taken.  This error is returned if the <i>dwIfIndex</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 transport is not configured on the local computer.

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

To retrieve the ARP table, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a> function. 

On Windows Vista and later, the <b>FlushIpNetTable</b> function can only be called by a user logged on as a member of the Administrators group. If <b>FlushIpNetTable</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista and later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  This function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipnetentry">CreateIpNetEntry</a>



<b>DeleteIpNetEntry</b>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiftable">GetIfTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>