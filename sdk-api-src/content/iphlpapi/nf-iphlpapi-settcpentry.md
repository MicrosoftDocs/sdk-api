---
UID: NF:iphlpapi.SetTcpEntry
title: SetTcpEntry function (iphlpapi.h)
description: The SetTcpEntry function sets the state of a TCP connection.
helpviewer_keywords: ["SetTcpEntry","SetTcpEntry function [IP Helper]","_iphlp_settcpentry","iphlp.settcpentry","iphlpapi/SetTcpEntry"]
old-location: iphlp\settcpentry.htm
tech.root: IpHlp
ms.assetid: 5916f66d-3c85-406d-b6f9-6c1c84161be4
ms.date: 12/05/2018
ms.keywords: SetTcpEntry, SetTcpEntry function [IP Helper], _iphlp_settcpentry, iphlp.settcpentry, iphlpapi/SetTcpEntry
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
 - SetTcpEntry
 - iphlpapi/SetTcpEntry
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
 - SetTcpEntry
---

# SetTcpEntry function


## -description

The 
<b>SetTcpEntry</b> function sets the state of a TCP connection.

## -parameters

### -param pTcpRow [in]

A pointer to a 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a> structure. This structure specifies information to identify the TCP connection to modify. It also specifies the new state for the TCP connection. The caller must specify values for all the members in this structure.

## -returns

The function returns <b>NO_ERROR</b> (zero) if the function is successful. 

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code/value</th>
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
An input parameter is invalid, no action was taken.  This error is returned if the <i>pTcpRow</i> parameter is <b>NULL</b> or the <b>Row</b> member in the <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a> structure pointed to by the <i>pTcpRow</i> parameter is not set to MIB_TCP_STATE_DELETE_TCB.

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
<dt>317</dt>
</dl>
</td>
<td width="60%">
 The function is unable to set the TCP entry since the application is running non-elevated.

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

Currently, the only state to which a TCP connection can be set is MIB_TCP_STATE_DELETE_TCB.

On Windows Vista and later, the <b>SetTcpEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetTcpEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>SetTcpEntry</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a>