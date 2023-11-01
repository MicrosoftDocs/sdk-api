---
UID: NF:lmjoin.NetProvisionComputerAccount
title: NetProvisionComputerAccount function (lmjoin.h)
description: Provisions a computer account for later use in an offline domain join operation.
helpviewer_keywords: ["NETSETUP_PROVISION_DOWNLEVEL_PRIV_SUPPORT","NETSETUP_PROVISION_REUSE_ACCOUNT","NETSETUP_PROVISION_ROOT_CA_CERTS","NETSETUP_PROVISION_SKIP_ACCOUNT_SEARCH","NETSETUP_PROVISION_USE_DEFAULT_PASSWORD","NetProvisionComputerAccount","NetProvisionComputerAccount function [Network Management]","Offline Domain Join","lmjoin/NetProvisionComputerAccount","netmgmt.netprovisioncomputeraccount"]
old-location: netmgmt\netprovisioncomputeraccount.htm
tech.root: NetMgmt
ms.assetid: 4c854258-b84d-4ef3-a6da-ce0a9540ffd5
ms.date: 12/05/2018
ms.keywords: NETSETUP_PROVISION_DOWNLEVEL_PRIV_SUPPORT, NETSETUP_PROVISION_REUSE_ACCOUNT, NETSETUP_PROVISION_ROOT_CA_CERTS, NETSETUP_PROVISION_SKIP_ACCOUNT_SEARCH, NETSETUP_PROVISION_USE_DEFAULT_PASSWORD, NetProvisionComputerAccount, NetProvisionComputerAccount function [Network Management], Offline Domain Join, lmjoin/NetProvisionComputerAccount, netmgmt.netprovisioncomputeraccount
req.header: lmjoin.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetProvisionComputerAccount
 - lmjoin/NetProvisionComputerAccount
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
 - NetProvisionComputerAccount
---

# NetProvisionComputerAccount function


## -description

The
				<b>NetProvisionComputerAccount</b> function provisions a computer account for later use in an offline domain join operation.

## -parameters

### -param lpDomain [in]

A pointer to a <b>NULL</b>-terminated character string that specifies the name of the domain where the computer account is created.

### -param lpMachineName [in]

A pointer to a <b>NULL</b>-terminated character string that specifies the short name of the machine from which the computer account attribute sAMAccountName is derived by appending a '$'. This parameter must contain a valid DNS or NetBIOS machine name.

### -param lpMachineAccountOU [in, optional]

An optional pointer to a <b>NULL</b>-terminated character string that contains the RFC 1779 format name of the organizational unit (OU) where the computer account will be created. If you specify this parameter, the string must contain a full path, for example, OU=testOU,DC=domain,DC=Domain,DC=com. Otherwise, this parameter must be <b>NULL</b>.

If this parameter is <b>NULL</b>, the well known computer object container will be used as published in the domain.

### -param lpDcName [in, optional]

An optional pointer to a <b>NULL</b>-terminated character string that contains the name of the domain controller to target.

### -param dwOptions [in]

A set of bit flags that define provisioning options. This parameter can be one or more of the following values defined in the <i>Lmjoin.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_DOWNLEVEL_PRIV_SUPPORT"></a><a id="netsetup_provision_downlevel_priv_support"></a><dl>
<dt><b>NETSETUP_PROVISION_DOWNLEVEL_PRIV_SUPPORT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If the caller requires account creation by privilege, this option will cause a retry on failure using account creation functions enabling interoperability with domain controllers running on earlier versions of Windows. 

The <i>lpMachineAccountOU</i> is not supported when using downlevel privilege support.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_REUSE_ACCOUNT"></a><a id="netsetup_provision_reuse_account"></a><dl>
<dt><b>NETSETUP_PROVISION_REUSE_ACCOUNT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If the named account already exists, an attempt will be made to reuse the existing account. 

This option requires sufficient credentials for this operation (Domain Administrator or the object owner).

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_USE_DEFAULT_PASSWORD"></a><a id="netsetup_provision_use_default_password"></a><dl>
<dt><b>NETSETUP_PROVISION_USE_DEFAULT_PASSWORD</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Use the default machine account password which is the machine name in lowercase. This is largely to support the older unsecure join model where the pre-created account typically used this default password. 

<div class="alert"><b>Note</b>  Applications should avoid using this option if possible. This option as well as <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a> function with dwOptions set to NETSETUP_JOIN_UNSECURE for unsecure join should only be used on earlier versions of Windows. </div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_SKIP_ACCOUNT_SEARCH"></a><a id="netsetup_provision_skip_account_search"></a><dl>
<dt><b>NETSETUP_PROVISION_SKIP_ACCOUNT_SEARCH</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Do not try to find the account on any domain controller in the domain. This option makes the operation faster, but should only be used when the caller is certain that an account by the same name hasn't recently been created. 

This option is only valid when the <i>lpDcName</i> parameter is specified. When the prerequisites are met, this option allows for must faster provisioning useful for scenarios such as batch processing. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_ROOT_CA_CERTS"></a><a id="netsetup_provision_root_ca_certs"></a><dl>
<dt><b>NETSETUP_PROVISION_ROOT_CA_CERTS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
This option retrieves all of the root Certificate Authority certificates on the local machine and adds them to the provisioning package when no certificate template names are provided as part of the provisioning package (the <b>aCertTemplateNames</b> member of the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> struct passed in the  <i>pProvisioningParams</i> parameter to the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function is NULL).

<div class="alert"><b>Note</b>  This flag is only supported by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function on Windows 8, Windows Server 2012, and later.</div>
<div> </div>
</td>
</tr>
</table>

### -param pProvisionBinData [out, optional]

An optional pointer that will receive the opaque binary blob of serialized metadata required by <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a> function to complete an offline domain join, if the <b>NetProvisionComputerAccount</b> function completes successfully.  The data is returned as an opaque binary buffer which may be passed to <b>NetRequestOfflineDomainJoin</b> function.  

If this parameter is <b>NULL</b>, then <i>pProvisionTextData</i> parameter must not be <b>NULL</b>. If this parameter is not <b>NULL</b>, then the  <i>pProvisionTextData</i> parameter must be <b>NULL</b>.

### -param pdwProvisionBinDataSize [out, optional]

A pointer to a value that receives the size, in bytes, of the buffer returned in the <i>pProvisionBinData</i> parameter. 

This parameter must not be <b>NULL</b> if the <i>pProvisionBinData</i> parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> when the <i>pProvisionBinData</i> parameter is <b>NULL</b>.

### -param pProvisionTextData [out, optional]

An optional pointer that will receive the opaque binary blob of serialized metadata required by <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a> function to complete an offline domain join, if the <b>NetProvisionComputerAccount</b> function completes successfully.  The data is returned in string form for embedding in an unattended setup answer file.  

If this parameter is <b>NULL</b>, then the <i>pProvisionBinData</i> parameter must not be <b>NULL</b>. If this parameter is not <b>NULL</b>, then the <i>pProvisionBinData</i> parameter must be <b>NULL</b>.

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
Access is denied. This error is returned if the caller does not have sufficient privileges to complete the operation. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DOMAIN_ROLE</b></dt>
</dl>
</td>
<td width="60%">
This operation is only allowed for the Primary Domain Controller of the domain. This error is returned if a domain controller name was specified in the <i>lpDcName</i> parameter, but the computer specified could not be validated as a domain controller for the target domain specified in the <i>lpDomain</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>lpDomain</i> or <i>lpMachineName</i> parameter is <b>NULL</b>. This error is also returned if both the <i>pProvisionBinData</i> and <i>pProvisionTextData</i> parameters are <b>NULL</b>. 

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
The request is not supported. This error is returned if the <i>lpMachineAccountOU</i> parameter was specified and the domain controller is running on an earlier versions of Windows that does not support this parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>    NERR_DS8DCRequired</b></dt>
</dl>
</td>
<td width="60%">
The specified domain controller does not meet the version requirement for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>    NERR_LDAPCapableDCRequired</b></dt>
</dl>
</td>
<td width="60%">
This operation requires a domain controller which supports LDAP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserExists</b></dt>
</dl>
</td>
<td width="60%">
The account already exists in the domain and the NETSETUP_PROVISION_REUSE_ACCOUNT bit was not specified in the <i>dwOptions</i> parameter.

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

The <b>NetProvisionComputerAccount</b> function is supported on Windows 7 and Windows Server 2008 R2 for offline join operations.  On Windows 8 or Windows Server 2008 R2, it is recommended that the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function be used instead of the <b>NetProvisionComputerAccount</b> function.

The <b>NetProvisionComputerAccount</b> function is used to provision a computer account for later use in an offline domain join operation using the  <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a> function. The offline domain join scenario uses these functions as follows: <ul>
<li><b>NetProvisionComputerAccount</b>  is a provisioning function that is first called to perform the network operations necessary to create and configure the computer object in Active Directory. The output from the <b>NetProvisionComputerAccount</b> is an opaque binary blob of serialized metadata used for the next step. </li>
<li>
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>, an image initialization function,   is then called to inject the output from the <b>NetProvisionComputerAccount</b> provisioning function into a Windows operating system image to be used during installation.  </li>
</ul>Changes to Windows initialization code will detect this saved state and affect the local only portion of domain join. 

The <b>NetProvisionComputerAccount</b> function will create or reuse the machine account in the domain, collect all necessary metadata and return it in an opaque versioned binary blob or as text for embedding in an unattended setup answer file. The opaque binary blob can be consumed by the offline domain join request operation supplying all the necessary input to complete the domain join during first boot without any network operations (local state updates only). 

<b>Security Note:  </b>The blob returned by the <b>NetProvisionComputerAccount</b> function contains very sensitive data. It should be treated just as securely as a plaintext password. The blob contains the machine account password and other information about the domain, including the domain name, the name of a domain controller, and the security ID (SID) of the domain. If the blob is being transported physically or over the network, care must be taken to transport it securely. The design makes no provisions for securing this data.  This problem exists today with unattended setup answer files which can carry a number of secrets including domain user passwords. The caller must secure the blob and the unattended setup files. Solutions to this problem are varied. As an example, a pre-exchanged key could be used to encrypt a session between the consumer and provisioning entity enabling a secure transfer of the opaque blob.


The opaque blob returned in the  <i>pProvisionBinData</i> parameter by the <b>NetProvisionComputerAccount</b> function is versioned to allow interoperability and serviceability scenarios between different versions of Windows (joining client, provisioning machine, and domain controller). The offline join scenario currently does not limit the lifetime of the blob returned by the <b>NetProvisionComputerAccount</b> function.   

For offline domain joins, the access check performed depends on the configuration of the domain. Computer account creation is enabled using three methods:<ul>
<li>Domain administrators have rights to create computer accounts.</li>
<li>The SD on a container can delegate the rights to create computer accounts.</li>
<li>By default, authenticated users may create computer accounts by privilege. Authenticated users are limited to creating  a limited number of accounts that is specified as a quota on the domain (the default value is 10). For more information, see the <a href="/openspecs/windows_protocols/ms-ada2/6ba13b0c-1620-478c-b2ae-eca041f2e1c4">ms-DS-MachineAccountQuota</a> attribute in the Active Directory schema.</li>
</ul>


The <b>NetProvisionComputerAccount</b> function works only with a writable domain controller and does not function against a read-only domain controller.  Once provisioning is done against a writable domain controller and the account is replicated to a read-only domain controller, then the other portions of offline domain join operation do not require access to a domain controller.

If the <b>NetProvisionComputerAccount</b> function is successful, the pointer in the <i>pProvisionBinData</i> or <i>pProvisionTextData</i> parameter (depending on which was parameter was not <b>NULL</b>) is returned with the serialized data for use in an offline join operation or as text in an unattended setup file.  

For more information on offline domain join operations, see the <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>.

Joining (and unjoining) a computer to a domain using <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a> and <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a> can be performed only by a member of the Administrators local group on the target computer. Note that the domain administrator can set additional requirements for joining the domain using delegation and assignment of privileges.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetCreateProvisioningPackage</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>



<a href="/openspecs/windows_protocols/ms-ada2/6ba13b0c-1620-478c-b2ae-eca041f2e1c4">ms-DS-MachineAccountQuota</a>