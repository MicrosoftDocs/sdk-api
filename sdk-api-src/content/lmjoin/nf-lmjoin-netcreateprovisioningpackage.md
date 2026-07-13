---
UID: NF:lmjoin.NetCreateProvisioningPackage
title: NetCreateProvisioningPackage function (lmjoin.h)
description: Creates a provisioning package that provisions a computer account for later use in an offline domain join operation. The package may also contain information about certificates and policies to add to the machine during provisioning.
helpviewer_keywords: ["NetCreateProvisioningPackage","NetCreateProvisioningPackage function [Network Management]","aCertTemplateNames","aMachinePolicyNames","aMachinePolicyPaths","cCertTemplateNames","cMachinePolicyNames","cMachinePolicyPaths","dwProvisionOptions","dwVersion","lmjoin/NetCreateProvisioningPackage","lpDcName","lpDomain","lpMachineAccountOU","lpMachineName","netmgmt.netcreateprovisioningpackage"]
old-location: netmgmt\netcreateprovisioningpackage.htm
tech.root: NetMgmt
ms.assetid: 6E2A5578-8308-41E2-B5E9-5E34E9E76C0B
ms.date: 12/05/2018
ms.keywords: NetCreateProvisioningPackage, NetCreateProvisioningPackage function [Network Management], aCertTemplateNames, aMachinePolicyNames, aMachinePolicyPaths, cCertTemplateNames, cMachinePolicyNames, cMachinePolicyPaths, dwProvisionOptions, dwVersion, lmjoin/NetCreateProvisioningPackage, lpDcName, lpDomain, lpMachineAccountOU, lpMachineName, netmgmt.netcreateprovisioningpackage
req.header: lmjoin.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - NetCreateProvisioningPackage
 - lmjoin/NetCreateProvisioningPackage
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
 - NetCreateProvisioningPackage
---

# NetCreateProvisioningPackage function


## -description

The
				<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetCreateProvisioningPackage</a> function creates a provisioning package that provisions a computer account for later use in an offline domain join operation. The package may also contain information about certificates and policies to add to the machine during provisioning.

## -parameters

### -param pProvisioningParams [in]

A pointer to a <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> structure that contains information about the provisioning package.

The following values are defined for the members of this structure:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dwVersion"></a><a id="dwversion"></a><a id="DWVERSION"></a><dl>
<dt><b>dwVersion</b></dt>
</dl>
</td>
<td width="60%">
The version of Windows in the provisioning package. This member should use the following value defined in the <i>Lmjoin.h</i> header file:

NETSETUP_PROVISIONING_PARAMS_CURRENT_VERSION (0x00000001)

</td>
</tr>
<tr>
<td width="40%"><a id="lpDomain"></a><a id="lpdomain"></a><a id="LPDOMAIN"></a><dl>
<dt><b>lpDomain</b></dt>
</dl>
</td>
<td width="60%">
A pointer to a constant null-terminated character string that specifies the name of the domain where the computer account is created. 


 

</td>
</tr>
<tr>
<td width="40%"><a id="lpMachineName"></a><a id="lpmachinename"></a><a id="LPMACHINENAME"></a><dl>
<dt><b>lpMachineName</b></dt>
</dl>
</td>
<td width="60%">
A pointer to a constant null-terminated character string that specifies the short name of the machine from which the computer account attribute sAMAccountName is derived by appending a '$'. This parameter must contain a valid DNS or NetBIOS machine name.

</td>
</tr>
<tr>
<td width="40%"><a id="lpMachineAccountOU"></a><a id="lpmachineaccountou"></a><a id="LPMACHINEACCOUNTOU"></a><dl>
<dt><b>lpMachineAccountOU</b></dt>
</dl>
</td>
<td width="60%">
An optional pointer to a constant null-terminated character string that contains the RFC 1779 format name of the organizational unit (OU) where the computer account will be created. If you specify this parameter, the string must contain a full path, for example, OU=testOU,DC=domain,DC=Domain,DC=com. Otherwise, this parameter must be <b>NULL</b>.

If this parameter is <b>NULL</b>, the well known computer object container will be used as published in the domain.

</td>
</tr>
<tr>
<td width="40%"><a id="lpDcName"></a><a id="lpdcname"></a><a id="LPDCNAME"></a><dl>
<dt><b>lpDcName</b></dt>
</dl>
</td>
<td width="60%">
An optional pointer to a constant null-terminated character string that contains the name of the domain controller to target.

</td>
</tr>
<tr>
<td width="40%"><a id="dwProvisionOptions"></a><a id="dwprovisionoptions"></a><a id="DWPROVISIONOPTIONS"></a><dl>
<dt><b>dwProvisionOptions</b></dt>
</dl>
</td>
<td width="60%">
A set of bit flags that define provisioning options. This parameter can be one or more of the values specified for the <i>dwOptions</i> parameter passed to the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function. 

These possible values are defined in the <i>Lmjoin.h</i> header file. 

The <b>NETSETUP_PROVISION_ROOT_CA_CERTS</b> option is only supported on Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="aCertTemplateNames"></a><a id="acerttemplatenames"></a><a id="ACERTTEMPLATENAMES"></a><dl>
<dt><b>aCertTemplateNames</b></dt>
</dl>
</td>
<td width="60%">
A optional pointer to an array of <b>NULL</b>-terminated certificate template names. 

</td>
</tr>
<tr>
<td width="40%"><a id="cCertTemplateNames"></a><a id="ccerttemplatenames"></a><a id="CCERTTEMPLATENAMES"></a><dl>
<dt><b>cCertTemplateNames</b></dt>
</dl>
</td>
<td width="60%">
When <b>aCertTemplateNames</b> is not NULL, this member provides an explicit count of the number of items in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="aMachinePolicyNames"></a><a id="amachinepolicynames"></a><a id="AMACHINEPOLICYNAMES"></a><dl>
<dt><b>aMachinePolicyNames</b></dt>
</dl>
</td>
<td width="60%">
An optional pointer to an array of <b>NULL</b>-terminated machine policy names.

</td>
</tr>
<tr>
<td width="40%"><a id="cMachinePolicyNames"></a><a id="cmachinepolicynames"></a><a id="CMACHINEPOLICYNAMES"></a><dl>
<dt><b>cMachinePolicyNames</b></dt>
</dl>
</td>
<td width="60%">
When <b>aMachinePolicyNames</b> is not <b>NULL</b>, this member provides an explicit count of the number of items in the array.

</td>
</tr>
<tr>
<td width="40%"><a id="aMachinePolicyPaths"></a><a id="amachinepolicypaths"></a><a id="AMACHINEPOLICYPATHS"></a><dl>
<dt><b>aMachinePolicyPaths</b></dt>
</dl>
</td>
<td width="60%">
An optional pointer to an array of  character strings. Each array element is a NULL-terminated character string which specifies the full or partial path to a file in the Registry Policy File format. For more information on the Registry Policy File Format , see <a href="/previous-versions/windows/desktop/Policy/registry-policy-file-format">Registry Policy File Format</a>


The path could
                     be a UNC path on a remote server.

</td>
</tr>
<tr>
<td width="40%"><a id="cMachinePolicyPaths"></a><a id="cmachinepolicypaths"></a><a id="CMACHINEPOLICYPATHS"></a><dl>
<dt><b>cMachinePolicyPaths</b></dt>
</dl>
</td>
<td width="60%">
When <b>aMachinePolicyPaths</b> is not <b>NULL</b>, this member provides an explicit count of the number of items in the array.

</td>
</tr>
</table>

### -param ppPackageBinData [out, optional]

An optional pointer that will receive the package required by <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a> function to complete an offline domain join, if the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function completes successfully.  The data is returned as an opaque binary buffer which may be passed to <b>NetRequestOfflineDomainJoin</b> function.  

If this parameter is <b>NULL</b>, then <i>pPackageTextData</i> parameter must not be <b>NULL</b>. If this parameter is not <b>NULL</b>, then the  <i>pPackageTextData</i> parameter must be <b>NULL</b>.

### -param pdwPackageBinDataSize [out, optional]

A pointer to a value that receives the size, in bytes, of the buffer returned in the <i>pProvisionBinData</i> parameter. 

This parameter must not be <b>NULL</b> if the <i>pPackageBinData</i> parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> when the <i>pPackageBinData</i> parameter is <b>NULL</b>.

### -param ppPackageTextData [out, optional]

An optional pointer that will receive the package required by <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a> function to complete an offline domain join, if the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function completes successfully.  The data is returned in string form for embedding in an unattended setup answer file.  

If this parameter is <b>NULL</b>, then the <i>pPackageBinData</i> parameter must not be <b>NULL</b>. If this parameter is not <b>NULL</b>, then the <i>pPackageBinData</i> parameter must be <b>NULL</b>.

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
This operation is only allowed for the Primary Domain Controller of the domain. This error is returned if a domain controller name was specified in the <b>lpDcName </b> of the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> struct pointed to by the <i>pProvisioningParams</i> parameter, but the computer specified could not be validated as a domain controller for the target domain specified in the <b>lpDomain</b> of the <b>NETSETUP_PROVISIONING_PARAMS</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is also returned if both the <i>pProvisioningParams</i> parameter is  <b>NULL</b>. This error is also returned if the <b>lpDomain</b> or <b>lpMachineName</b> member of the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> struct pointed to by the <i>pProvisioningParams</i> parameter is <b>NULL</b>. 

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
The request is not supported. This error is returned if the <b>lpMachineAccountOU</b> member was specified in the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> struct pointed to by the <i>pProvisioningParams</i> parameter and the domain controller is running on an earlier versions of Windows that does not support this parameter.

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
The account already exists in the domain and the <b>NETSETUP_PROVISION_REUSE_ACCOUNT</b> bit was not specified in the <b>dwProvisionOptions</b> member of the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a> struct pointed to by the <i>pProvisioningParams</i> parameter.

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

The <b>NetCreateProvisioningPackage</b> function is supported on Windows 8 and  Windows Server 2012 for offline join operations.  For Windows 7, use the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function.

The <b>NetCreateProvisioningPackage</b> function is used to provision a computer account for later use in an offline domain join operation using the  <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a> function.

The offline domain join scenario uses two functions: <ul>
<li><b>NetCreateProvisioningPackage</b>  is a provisioning function that is first called to perform the network operations necessary to create and configure the computer object in Active Directory. The output from the <b>NetCreateProvisioningPackage</b> is a package used for the next step. </li>
<li>
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>, an image initialization function,   is called to inject the output from the <b>NetCreateProvisioningPackage</b> provisioning function into a Windows operating system image for use during pre-installation and post-installation. </li>
</ul>Changes to Windows initialization code will detect this saved state and affect the local-only portion of domain join.

When the <i>pPackageBinData</i> and <i>pdwPackageBinDataSize</i> out pointers are used, set the <i>pPackageTextData</i> out pointer to NULL. When <i>pPackageTextData</i> is used, set the <i>pPackageBinData</i> and <i>pdwPackageBinDataSize</i> out pointers to NULL.

The <i>pProvisioningParams</i> parameter specifies data to include in the provisioning package. The package includes information relevant to the domain join, and it can also include information about policies and certificates to install on the machine. The provisioning package can be used in four ways:<ul>
<li>Domain join</li>
<li>Domain join and installation of certificates</li>
<li>Domain join and installation of policies</li>
<li>Domain join and installation of certificates and policies</li>
</ul>


The <b>NetCreateProvisioningPackage</b> function creates or reuses the machine account in the domain, collects all necessary metadata and returns it in a package. The package can be consumed by the offline domain join request operation supplying all the necessary input to complete the domain join during first boot without any network operations (local state updates only). 

<b>Security Note:  </b>The package returned by the <b>NetCreateProvisioningPackage</b> function contains very sensitive data. It should be treated just as securely as a plaintext password. The package contains the machine account password and other information about the domain, including the domain name, the name of a domain controller, and the security ID (SID) of the domain. If the package is being transported physically or over the network, care must be taken to transport it securely. The design makes no provisions for securing this data.  This problem exists today with unattended setup answer files which can carry a number of secrets including domain user passwords. The caller must secure the package. Solutions to this problem are varied. As an example, a pre-exchanged key could be used to encrypt a session between the consumer and provisioning entity enabling a secure transfer of the package.


The package returned in the  <i>pPackageBinData</i> parameter by the <b>NetCreateProvisioningPackage</b> function is versioned to allow interoperability and serviceability scenarios between different versions of Windows (such as joining a client, provisioning a machine, and using a domain controller). A package created on Windows 8 or Windows Server 2012 can be used Windows 7 or Windows Server 2008 R2, however only domain join information will take effect (certificates and policies are not supported). The offline join scenario currently does not limit the lifetime of the package returned by the <b>NetCreateProvisioningPackage</b> function.

For offline domain joins, the access check performed depends on the configuration of the domain. Computer account creation is enabled using three methods:<ul>
<li>Domain administrators have rights to create computer accounts.</li>
<li>The SD on a container can delegate the rights to create computer accounts.</li>
<li>By default, authenticated users may create computer accounts by privilege. Authenticated users are limited to creating  a limited number of accounts that is specified as a quota on the domain (the default value is 10). For more information, see the <a href="/openspecs/windows_protocols/ms-ada2/6ba13b0c-1620-478c-b2ae-eca041f2e1c4">ms-DS-MachineAccountQuota</a> attribute in the Active Directory schema.</li>
</ul>


The <b>NetCreateProvisioningPackage</b> function works only with a writable domain controller and does not function against a read-only domain controller.  Once provisioning is done against a writable domain controller and the account is replicated to a read-only domain controller,  the other portions of the offline domain join operation do not require access to a domain controller.

If the <b>NetCreateProvisioningPackage</b> function is successful, the pointer in the <i>pPackageBinData</i> or <i>pPackageTextData</i> parameter (depending on which  parameter was not <b>NULL</b>) is returned with the serialized data for use in an offline join operation or as text in an unattended setup file.  

All phases of the provisioning process append to a  <i>NetSetup.log</i> file on the local computer. The provisioning process can include up to three different computers: the computer where the provisioning package is created,  the computer that requests the installation of the package,  and the computer where the  package is installed. There will be <i>NetSetup.log</i> file information stored on all three computers according to  the operation performed. Reviewing the contents of these files is the most common means of troubleshooting online and offline provisioning errors. Provisioning operations undertaken by admins are logged to the <i>NetSetup.log</i> file in the <i>%WINDIR%\Debug</i>. Provisioning operations performed by non-admins are logged to the <i>NetSetup.log</i> file  in the <i>%USERPROFILE%\Debug</i> folder.

For more information on offline domain join operations, see the <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>.

Joining (and unjoining) a computer to a domain using <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a> and <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a> is performed only by a member of the Administrators local group on the target computer. Note that the domain administrator can set additional requirements for joining the domain using delegation and assignment of privileges.

## -see-also

<a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>