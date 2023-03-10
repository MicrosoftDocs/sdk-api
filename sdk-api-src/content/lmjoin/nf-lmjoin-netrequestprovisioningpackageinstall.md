---
UID: NF:lmjoin.NetRequestProvisioningPackageInstall
title: NetRequestProvisioningPackageInstall function (lmjoin.h)
description: Executes locally on a machine to modify a Windows operating system image mounted on a volume. (NetRequestProvisioningPackageInstall)
helpviewer_keywords: ["NETSETUP_PROVISION_ONLINE_CALLER","NetRequestProvisioningPackageInstall","NetRequestProvisioningPackageInstall function [Network Management]","lmjoin/NetRequestProvisioningPackageInstall","netmgmt.netrequestprovisioningpackageinstall"]
old-location: netmgmt\netrequestprovisioningpackageinstall.htm
tech.root: NetMgmt
ms.assetid: 107ED0F7-8DDD-4C18-8C34-3A67F771FA62
ms.date: 12/05/2018
ms.keywords: NETSETUP_PROVISION_ONLINE_CALLER, NetRequestProvisioningPackageInstall, NetRequestProvisioningPackageInstall function [Network Management], lmjoin/NetRequestProvisioningPackageInstall, netmgmt.netrequestprovisioningpackageinstall
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
 - NetRequestProvisioningPackageInstall
 - lmjoin/NetRequestProvisioningPackageInstall
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
 - NetRequestProvisioningPackageInstall
---

# NetRequestProvisioningPackageInstall function


## -description

The
				<b>NetRequestProvisioningPackageInstall</b> function executes locally on a machine to modify a Windows operating system image mounted on a volume. The registry is loaded from the image and provisioning package data is written where it can be retrieved during the completion phase of an offline domain join operation.

## -parameters

### -param pPackageBinData [in]

A pointer to a buffer required to initialize the registry of a Windows operating system image to process the final local state change during the completion phase of the offline domain join operation. 

The opaque binary blob of serialized metadata passed in the <i>pPackageBinData</i> parameter is returned by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetCreateProvisioningPackage</a> function.

### -param dwPackageBinDataSize [in]

The size, in bytes, of the buffer pointed to by the <i>pPackageBinData</i> parameter. 

This parameter must not be <b>NULL</b>.

### -param dwProvisionOptions [in]

A set of bit flags that define options for this function.  This parameter uses one or more of the following values defined in the <i>Lmjoin.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISION_ONLINE_CALLER"></a><a id="netsetup_provision_online_caller"></a><dl>
<dt><b>NETSETUP_PROVISION_ONLINE_CALLER</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
This flag is required if the <i>lpWindowsPath</i> parameter references the currently running Windows operating system directory rather than an offline Windows operating system image mounted on an accessible volume. If this flag is specified,  the <b>NetRequestProvisioningPackageInstall</b>  function must be invoked by a member of the local Administrators group.

</td>
</tr>
</table>

### -param lpWindowsPath [in]

A pointer to a <b>NULL</b>-terminated character string that specifies the path to a Windows operating system image  under which the registry hives are located. This image must be offline and not currently booted unless the <i>dwProvisionOptions</i> parameter contains <b>NETSETUP_PROVISION_ONLINE_CALLER</b>, in which case, the locally running operating system directory is allowed. 

This path could
                     be a UNC path on a remote server.

### -param pvReserved

Reserved for future use.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following <a href="/windows/desktop/NetMgmt/network-management-error-codes">Network Management error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NoOfflineJoinInfo </b></dt>
</dl>
</td>
<td width="60%">
The offline join completion information was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BadOfflineJoinInfo</b></dt>
</dl>
</td>
<td width="60%">
The offline join completion information was bad.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_CantCreateJoinInfo</b></dt>
</dl>
</td>
<td width="60%">
Unable to create offline join information. Please ensure you have access to the specified path location and permissions to modify its contents. Running as an elevated administrator may be required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BadDomainJoinInfo</b></dt>
</dl>
</td>
<td width="60%">
The domain join info being saved was incomplete or bad.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_JoinPerformedMustRestart</b></dt>
</dl>
</td>
<td width="60%">
Offline join operation successfully completed but a restart is needed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NoJoinPending</b></dt>
</dl>
</td>
<td width="60%">
There was no offline join operation pending.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ValuesNotSet</b></dt>
</dl>
</td>
<td width="60%">
Unable to set one or more requested machine or domain name values on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_CantVerifyHostname</b></dt>
</dl>
</td>
<td width="60%">
Could not verify the current machine's hostname against the saved value in the join completion information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_CantLoadOfflineHive</b></dt>
</dl>
</td>
<td width="60%">
Unable to load the specified offline registry hive. Please ensure you have access to the specified path location and permissions to modify its contents. Running as an elevated administrator may be required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ConnectionInsecure</b></dt>
</dl>
</td>
<td width="60%">
The minimum session security requirements for this operation were not met.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ProvisioningBlobUnsupported</b></dt>
</dl>
</td>
<td width="60%">
Computer account provisioning blob version is not supported.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestProvisioningPackageInstall</a> function is supported on Windows 8 for offline domain join operations.  For  Windows 7, use <b>NetRequestOfflineDomainJoin</b>.

The offline domain join scenario uses two functions: <ul>
<li>
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a>  is a provisioning function that is first called to perform the network operations necessary to create and configure the computer object in Active Directory. The output from the <b>NetCreateProvisioningPackage</b> is a package used for the next step. </li>
<li><b>NetRequestProvisioningPackageInstall</b>, an image initialization function,   is called to inject the output from the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> provisioning function into a Windows operating system image for use during installation. </li>
</ul>Changes to Windows initialization code will detect this saved state and affect the local-only portion of domain join and install any certificate and  policy information that may have been present in the package.

The <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function will create or reuse the machine account in the domain, collect all necessary metadata and return it in a package. The package can be consumed by the offline domain join request operation supplying all the necessary input to complete the domain join during first boot without any network operations (local state updates only). 

<b>Security Note:  </b>The package created by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function contains very sensitive data. It should be treated just as securely as a plaintext password. The package contains the machine account password and other information about the domain, including the domain name, the name of a domain controller, and the security ID (SID) of the domain. If the package is being transported physically or over the network, care must be taken to transport it securely. The design makes no provisions for securing this data.  This problem exists today with unattended setup answer files which can carry a number of secrets including domain user passwords. The caller must secure the package. Solutions to this problem are varied. As an example, a pre-exchanged key could be used to encrypt a session between the consumer and provisioning entity enabling a secure transfer of the package.


The package returned in the  <i>pPackageBinData</i> parameter by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a> function is versioned to allow interoperability and serviceability scenarios between different versions of Windows (such as joining a client, provisioning a machine, and using a domain controller). The offline join scenario currently does not limit the lifetime of the package returned by the <b>NetCreateProvisioningPackage</b> function.

All phases of the provisioning process append to a  <i>NetSetup.log</i> file on the local computer. The provisioning process can include up to three different computers: the computer where the provisioning package is created,  the computer that requests the installation of the package,  and the computer where the  package is installed. There will be <i>NetSetup.log</i> file information stored on all three computers according to  the operation performed. Reviewing the contents of these files is the most common means of troubleshooting online and offline provisioning errors. Provisioning operations undertaken by admins are logged to the <i>NetSetup.log</i> file in the <i>%WINDIR%\Debug</i>. Provisioning operations performed by non-admins are logged to the <i>NetSetup.log</i> file  in the <i>%USERPROFILE%\Debug</i> folder.

## -see-also

<a href="/windows/desktop/api/lmjoin/ns-lmjoin-netsetup_provisioning_params">NETSETUP_PROVISIONING_PARAMS</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetCreateProvisioningPackage</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<b>NetProvisionComputerAccount</b>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>
