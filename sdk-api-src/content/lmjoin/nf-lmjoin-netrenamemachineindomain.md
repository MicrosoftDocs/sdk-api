---
UID: NF:lmjoin.NetRenameMachineInDomain
title: NetRenameMachineInDomain function (lmjoin.h)
description: The NetRenameMachineInDomain function changes the name of a computer in a domain.
helpviewer_keywords: ["NetRenameMachineInDomain","NetRenameMachineInDomain function [Network Management]","_win32_netrenamemachineindomain","lmjoin/NetRenameMachineInDomain","netmgmt.netrenamemachineindomain"]
old-location: netmgmt\netrenamemachineindomain.htm
tech.root: NetMgmt
ms.assetid: 1f7ddaa1-a349-49a6-856d-a2fde2f1dc3b
ms.date: 12/05/2018
ms.keywords: NetRenameMachineInDomain, NetRenameMachineInDomain function [Network Management], _win32_netrenamemachineindomain, lmjoin/NetRenameMachineInDomain, netmgmt.netrenamemachineindomain
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
 - NetRenameMachineInDomain
 - lmjoin/NetRenameMachineInDomain
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
 - NetRenameMachineInDomain
---

# NetRenameMachineInDomain function


## -description

The 
				<b>NetRenameMachineInDomain</b> function changes the name of a computer in a domain.

## -parameters

### -param lpServer [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpNewMachineName [in]

A pointer to a constant string that specifies the new name of the computer. If specified, the local computer name is changed as well. If this parameter is <b>NULL</b>, the function assumes you have already called the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> function.

### -param lpAccount [in]

A pointer to a constant string that specifies an account name to use when connecting to the domain controller. If this parameter is <b>NULL</b>, the caller's context is used.

### -param lpPassword [in]

If the <i>lpAccount</i> parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>.

### -param fRenameOptions [in]

The rename options. If this parameter is NETSETUP_ACCT_CREATE, the function renames the account in the domain.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned if the account name passed in the <i>lpAccount</i> parameter did not have sufficient access rights for the operation. 

</td>
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

Renaming a domain computer can be performed only by a user that is a member of the Administrators local group on the target computer and that also is a member of the Administrators group on the domain or has the Account Operator privilege on the domain. If you call the 
<b>NetRenameMachineInDomain</b> function remotely, you must supply credentials because you cannot delegate credentials under these circumstances.

Different processes, or different threads of the same process, should not call the 
<b>NetRenameMachineInDomain</b> function at the same time. This situation can leave the computer in an inconsistent state.

The <b>NERR_SetupNotJoined</b> and  <b>NERR_SetupDomainController</b> return values are defined in the Lmerr.h header file. This header file is automatically included by the Lm.h header file and should not be included directly.

A system reboot is required after calling the <b>NetRenameMachineInDomain</b> function for the operation to complete.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netaddalternatecomputername">NetAddAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netenumeratecomputernames">NetEnumerateComputerNames</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netremovealternatecomputername">NetRemoveAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netsetprimarycomputername">NetSetPrimaryComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>