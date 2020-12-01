---
UID: NF:lmjoin.NetJoinDomain
title: NetJoinDomain function (lmjoin.h)
description: The NetJoinDomain function joins a computer to a workgroup or domain.
helpviewer_keywords: ["NETSETUP_ACCT_CREATE","NETSETUP_AMBIGUOUS_DC","NETSETUP_DEFER_SPN_SET","NETSETUP_DOMAIN_JOIN_IF_JOINED","NETSETUP_DONT_CONTROL_SERVICES","NETSETUP_FORCE_SPN_SET","NETSETUP_IGNORE_UNSUPPORTED_FLAGS","NETSETUP_JOIN_DC_ACCOUNT","NETSETUP_JOIN_DOMAIN","NETSETUP_JOIN_READONLY","NETSETUP_JOIN_UNSECURE","NETSETUP_JOIN_WITH_NEW_NAME","NETSETUP_MACHINE_PWD_PASSED","NETSETUP_NO_ACCT_REUSE","NETSETUP_NO_NETLOGON_CACHE","NETSETUP_SET_MACHINE_NAME","NETSETUP_WIN9X_UPGRADE","NetJoinDomain","NetJoinDomain function [Network Management]","_win32_netjoindomain","lmjoin/NetJoinDomain","netmgmt.netjoindomain"]
old-location: netmgmt\netjoindomain.htm
tech.root: NetMgmt
ms.assetid: 4efcb399-03af-4312-9f1d-6bc38f356cac
ms.date: 12/05/2018
ms.keywords: NETSETUP_ACCT_CREATE, NETSETUP_AMBIGUOUS_DC, NETSETUP_DEFER_SPN_SET, NETSETUP_DOMAIN_JOIN_IF_JOINED, NETSETUP_DONT_CONTROL_SERVICES, NETSETUP_FORCE_SPN_SET, NETSETUP_IGNORE_UNSUPPORTED_FLAGS, NETSETUP_JOIN_DC_ACCOUNT, NETSETUP_JOIN_DOMAIN, NETSETUP_JOIN_READONLY, NETSETUP_JOIN_UNSECURE, NETSETUP_JOIN_WITH_NEW_NAME, NETSETUP_MACHINE_PWD_PASSED, NETSETUP_NO_ACCT_REUSE, NETSETUP_NO_NETLOGON_CACHE, NETSETUP_SET_MACHINE_NAME, NETSETUP_WIN9X_UPGRADE, NetJoinDomain, NetJoinDomain function [Network Management], _win32_netjoindomain, lmjoin/NetJoinDomain, netmgmt.netjoindomain
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
 - NetJoinDomain
 - lmjoin/NetJoinDomain
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
 - NetJoinDomain
---

# NetJoinDomain function


## -description

The
				<b>NetJoinDomain</b> function joins a computer to a workgroup or domain.

## -parameters

### -param lpServer [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to execute the domain join operation. If this parameter is <b>NULL</b>, the local computer is used.

### -param lpDomain [in]

A pointer to a constant null-terminated character string that specifies the name of the domain or workgroup to join. 




Optionally, you can specify the preferred domain controller to perform the join operation. In this instance, the string must be of the form  <i>DomainName\MachineName</i>,  where <i>DomainName</i>  is the name of the domain to join, and <i>MachineName</i> is the name of the domain controller to perform the join.

### -param lpMachineAccountOU [in]

Optionally specifies the pointer to a constant null-terminated character string that contains the RFC 1779 format name of the organizational unit (OU) for the computer account. If you specify this parameter, the string must contain a full path, for example, OU=testOU,DC=domain,DC=Domain,DC=com. Otherwise, this parameter must be <b>NULL</b>.

### -param lpAccount [in]

A pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller. The string must specify either a domain NetBIOS name and user account (for example, <i>REDMOND\user</i>) or the user principal name (UPN) of the user in the form of an Internet-style login name (for example, "someone@example.com"). If this parameter is <b>NULL</b>, the caller's context is used.

### -param lpPassword [in]

If the <i>lpAccount</i> parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>. 




You can specify a local machine account password rather than a user password for unsecured joins. For more information, see the description of the NETSETUP_MACHINE_PWD_PASSED flag described in the <i>fJoinOptions</i> parameter.

### -param fJoinOptions [in]

A set of bit flags defining the join options. This parameter can be one or more of the following values defined in the <i>Lmjoin.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_JOIN_DOMAIN"></a><a id="netsetup_join_domain"></a><dl>
<dt><b>NETSETUP_JOIN_DOMAIN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Joins the computer to a domain. If this value is not specified, joins the computer to a workgroup.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_ACCT_CREATE"></a><a id="netsetup_acct_create"></a><dl>
<dt><b>NETSETUP_ACCT_CREATE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Creates the account on the domain.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_WIN9X_UPGRADE"></a><a id="netsetup_win9x_upgrade"></a><dl>
<dt><b>NETSETUP_WIN9X_UPGRADE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The join operation is occurring as part of an upgrade.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></a><a id="netsetup_domain_join_if_joined"></a><dl>
<dt><b>NETSETUP_DOMAIN_JOIN_IF_JOINED</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Allows a join to a new domain even if the computer is already joined to a domain.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_JOIN_UNSECURE"></a><a id="netsetup_join_unsecure"></a><dl>
<dt><b>NETSETUP_JOIN_UNSECURE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Performs an unsecured join. 

This option requests a domain join to a pre-created account without authenticating with domain user credentials. This option can be used in conjunction with <b>NETSETUP_MACHINE_PWD_PASSED</b> option.  In this case, <i>lpPassword</i> is the password of the pre-created machine account. 

Prior to Windows Vista with SP1 and  Windows Server 2008, an unsecure join did not authenticate to the domain controller. All communication was performed using a null (unauthenticated) session. Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_MACHINE_PWD_PASSED"></a><a id="netsetup_machine_pwd_passed"></a><dl>
<dt><b>NETSETUP_MACHINE_PWD_PASSED</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
 Indicates that the <i>lpPassword</i> parameter specifies a local machine account password rather than a user password. This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP_JOIN_UNSECURE flag.

If you set this flag, then after the join operation succeeds, the machine password will be set to the value of <i>lpPassword</i>, if that value is a valid machine password.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_DEFER_SPN_SET"></a><a id="netsetup_defer_spn_set"></a><dl>
<dt><b>NETSETUP_DEFER_SPN_SET</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time. 

Typically, these properties are updated during the join operation. Instead, these properties should be updated during a subsequent call to the 
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a> function. These properties are always updated during the rename operation. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_JOIN_DC_ACCOUNT"></a><a id="netsetup_join_dc_account"></a><dl>
<dt><b>NETSETUP_JOIN_DC_ACCOUNT</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Allow the domain join if existing account is a domain controller.

<div class="alert"><b>Note</b>  This flag is supported on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_JOIN_WITH_NEW_NAME"></a><a id="netsetup_join_with_new_name"></a><dl>
<dt><b>NETSETUP_JOIN_WITH_NEW_NAME</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Join the target machine specified in <i>lpServer</i> parameter with a new name queried from the registry on the machine specified in the <i>lpServer</i> parameter. 

This option is used if <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> has been called prior to rebooting the machine. The new computer name will not take effect until a reboot. With this option, the caller instructs the <b>NetJoinDomain</b> function to use the new name during the domain join operation. A reboot is required after calling <b>NetJoinDomain</b> successfully at which time both the computer name change and domain membership change will have taken affect.  

<div class="alert"><b>Note</b>  This flag is supported on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_JOIN_READONLY"></a><a id="netsetup_join_readonly"></a><dl>
<dt><b>NETSETUP_JOIN_READONLY</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Join the target machine specified in <i>lpServer</i> parameter using a pre-created account without requiring a writable domain controller. 

This option provides the ability to join a machine to domain if an account has already been provisioned and replicated to  a read-only domain controller. The target read-only domain controller is specified as part of the <i>lpDomain</i> parameter, after the domain name delimited by a ‘\’ character. This provisioning must include the machine secret. The machine account must be added via group membership into the allowed list for password replication policy, and the account password must be replicated to the read-only domain controller prior to the join operation. For more information, see the information on <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753470(v=ws.10)">Password Replication Policy Administration</a>.

Starting with Windows 7, an alternate mechanism is to use the offline domain join mechanism. For more information, see the <b>NetProvisionComputerAccount</b> and <b>NetRequestOfflineDomainJoin</b> functions.

<div class="alert"><b>Note</b>  This flag is supported on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_AMBIGUOUS_DC"></a><a id="netsetup_ambiguous_dc"></a><dl>
<dt><b>NETSETUP_AMBIGUOUS_DC</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
When joining the domain don't try to set the
                                                preferred domain controller in the registry.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_NO_NETLOGON_CACHE"></a><a id="netsetup_no_netlogon_cache"></a><dl>
<dt><b>NETSETUP_NO_NETLOGON_CACHE</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
When joining the domain don't create the Netlogon cache.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_DONT_CONTROL_SERVICES"></a><a id="netsetup_dont_control_services"></a><dl>
<dt><b>NETSETUP_DONT_CONTROL_SERVICES</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
When joining the domain don't force Netlogon service  to start.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_SET_MACHINE_NAME"></a><a id="netsetup_set_machine_name"></a><dl>
<dt><b>NETSETUP_SET_MACHINE_NAME</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
When joining the domain for offline join only, set target machine hostname and NetBIOS name.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_FORCE_SPN_SET"></a><a id="netsetup_force_spn_set"></a><dl>
<dt><b>NETSETUP_FORCE_SPN_SET</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
When joining the domain, override other settings during domain join and set the service principal name (SPN).

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_NO_ACCT_REUSE"></a><a id="netsetup_no_acct_reuse"></a><dl>
<dt><b>NETSETUP_NO_ACCT_REUSE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
When joining the domain, do not reuse an existing account.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></a><a id="netsetup_ignore_unsupported_flags"></a><dl>
<dt><b>NETSETUP_IGNORE_UNSUPPORTED_FLAGS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
If this bit is set, unrecognized flags
                                                       will be ignored by the <b>NetJoinDomain</b> function and  <b>NetJoinDomain</b> will behave as if the flags
                                                       were not set.

</td>
</tr>
</table>

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
Access is denied. This error is returned if the caller was not a member of the Administrators local group on the target computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>lpDomain</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The specified domain did not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the computer specified in the <i>lpServer</i> parameter does not support  some of the options passed in the <i>fJoinOptions</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidWorkgroupName</b></dt>
</dl>
</td>
<td width="60%">
The specified workgroup name is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SetupAlreadyJoined</b></dt>
</dl>
</td>
<td width="60%">
The computer is already joined to a domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_WkstaNotStarted</b></dt>
</dl>
</td>
<td width="60%">
The Workstation service has not been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A remote procedure call is already in progress for this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The remote procedure call protocol sequence is not supported.

</td>
</tr>
</table>

## -remarks

Joining (and unjoining) a computer to a domain or workgroup can be performed only by a member of the Administrators local group on the target computer. Note that the domain administrator can set additional requirements for joining the domain using delegation and assignment of privileges.

If you call the 
<b>NetJoinDomain</b> function remotely, you must supply credentials because you cannot delegate credentials under these circumstances.

Different processes, or different threads of the same process, should not call the 
<b>NetJoinDomain</b> function at the same time. This situation can leave the computer in an inconsistent state.

If you encounter a problem during a join operation, you should not delete a computer account and immediately follow the deletion with another join attempt. This can lead to replication-related problems that are difficult to investigate. When you delete a computer account, wait until the change has replicated to all domain controllers before attempting another join operation.

A system reboot is required after calling the <b>NetJoinDomain</b> function for the operation to complete.

<b>Windows Server 2003 and Windows XP:  </b>When a call to the 
<b>NetJoinDomain</b> function precedes a call to the 
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a> function, you should defer the update of the SPN and DnsHostName properties on the computer object until the rename operation. This is because the join operation can fail in certain situations. An example of such a situation is when the SPN that is derived from the current computer name is not valid in the new domain that the computer is joining, but the SPN derived from the new name that the computer will have after the rename operation is valid in the new domain. In this situation, the call to 
<b>NetJoinDomain</b> fails unless you defer the update of the two properties until the rename operation by specifying the NETSETUP_DEFER_SPN_SET flag in the <i>fJoinOptions</i> parameter when you call 
<b>NetJoinDomain</b>.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netaddalternatecomputername">NetAddAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netenumeratecomputernames">NetEnumerateComputerNames</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netremovealternatecomputername">NetRemoveAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netsetprimarycomputername">NetSetPrimaryComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753470(v=ws.10)">Password Replication Policy Administration</a>