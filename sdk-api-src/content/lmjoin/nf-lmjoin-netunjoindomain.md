---
UID: NF:lmjoin.NetUnjoinDomain
title: NetUnjoinDomain function (lmjoin.h)
description: The NetUnjoinDomain function unjoins a computer from a workgroup or a domain.
helpviewer_keywords: ["NetUnjoinDomain","NetUnjoinDomain function [Network Management]","_win32_netunjoindomain","lmjoin/NetUnjoinDomain","netmgmt.netunjoindomain"]
old-location: netmgmt\netunjoindomain.htm
tech.root: NetMgmt
ms.assetid: cc755c22-1fd6-4787-999e-a43258287a05
ms.date: 12/05/2018
ms.keywords: NetUnjoinDomain, NetUnjoinDomain function [Network Management], _win32_netunjoindomain, lmjoin/NetUnjoinDomain, netmgmt.netunjoindomain
req.header: lmjoin.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetUnjoinDomain
 - lmjoin/NetUnjoinDomain
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
 - NetUnjoinDomain
---

# NetUnjoinDomain function


## -description

The
				<b>NetUnjoinDomain</b> function unjoins a computer from a workgroup or a domain.

## -parameters

### -param lpServer [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpAccount [in]

A pointer to a constant string that specifies the account name to use when connecting to the domain controller. The string must specify either a domain NetBIOS name and user account (for example, <i>REDMOND\user</i>) or the user principal name (UPN) of the user in the form of an Internet-style login name (for example, "someone@example.com"). If this parameter is <b>NULL</b>, the caller's context is used.

### -param lpPassword [in]

If the <i>lpAccount</i> parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>.

### -param fUnjoinOptions [in]

Specifies the unjoin options. If this parameter is NETSETUP_ACCT_DELETE, the account is disabled when the unjoin occurs. Note that this option does not delete the account. Currently, there are no other unjoin options defined.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes or one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SetupNotJoined</b></dt>
</dl>
</td>
<td width="60%">
The computer is not currently joined to a domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SetupDomainController</b></dt>
</dl>
</td>
<td width="60%">
This computer is a domain controller and cannot be unjoined from a domain.

</td>
</tr>
</table>

## -remarks

Unjoining (and joining) a computer to a domain or workgroup can be performed only by a member of the Administrators local group on the target computer. If you call the 
<b>NetUnjoinDomain</b> function remotely, you must supply credentials because you cannot delegate credentials under these circumstances.

Different processes, or different threads of the same process, should not call the 
<b>NetUnjoinDomain</b> function at the same time. This situation can leave the computer in an inconsistent state.

A system reboot is required after calling the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a> function for the operation to complete.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>