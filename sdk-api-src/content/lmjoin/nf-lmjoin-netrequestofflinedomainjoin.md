---
UID: NF:lmjoin.NetRequestOfflineDomainJoin
title: NetRequestOfflineDomainJoin function (lmjoin.h)
description: Executes locally on a machine to modify a Windows operating system image mounted on a volume. (NetRequestOfflineDomainJoin)
helpviewer_keywords: ["NETSETUP_PROVISION_ONLINE_CALLER","NetRequestOfflineDomainJoin","NetRequestOfflineDomainJoin function [Network Management]","lmjoin/NetRequestOfflineDomainJoin","netmgmt.netrequestofflinedomainjoin"]
old-location: netmgmt\netrequestofflinedomainjoin.htm
tech.root: NetMgmt
ms.assetid: f3f8fe00-d6f7-4d59-a4e7-6aef7f507e1a
ms.date: 12/05/2018
ms.keywords: NETSETUP_PROVISION_ONLINE_CALLER, NetRequestOfflineDomainJoin, NetRequestOfflineDomainJoin function [Network Management], lmjoin/NetRequestOfflineDomainJoin, netmgmt.netrequestofflinedomainjoin
req.header: lmjoin.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - NetRequestOfflineDomainJoin
 - lmjoin/NetRequestOfflineDomainJoin
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
 - NetRequestOfflineDomainJoin
---

# NetRequestOfflineDomainJoin function


## -description

The
				<b>NetRequestOfflineDomainJoin</b> function executes locally on a machine to modify a Windows operating system image mounted on a volume. The registry is loaded from the image and provisioning blob data is written where it can be retrieved during the completion phase of an offline domain join operation.

## -parameters

### -param pProvisionBinData [in]

A pointer to a buffer required to initialize the registry of a Windows operating system image to process the final local state change during the completion phase of the offline domain join operation. 

The opaque binary blob of serialized metadata passed in the <i>pProvisionBinData</i> parameter is returned by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function.

### -param cbProvisionBinDataSize [in]

The size, in bytes, of the buffer pointed to by the <i>pProvisionBinData</i> parameter. 

This parameter must not be <b>NULL</b>.

### -param dwOptions [in]

A set of bit flags that define options for this function. This parameter can be one or more of the following values defined in the <i>Lmjoin.h</i> header file. 



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
This flag is required if the <i>lpWindowsPath</i> parameter references the currently running Windows operating system directory rather than an offline Windows operating system image mounted on an accessible volume. If this flag is specified,  the <b>NetRequestOfflineDomainJoin</b> function must be invoked by a member of the local Administrators group.

</td>
</tr>
</table>

### -param lpWindowsPath [in]

A pointer to a constant null-terminated character string that specifies the path to a Windows operating system image  under which the registry hives are located. This image must be offline and not currently booted unless the <i>dwOptions</i> parameter contains <b>NETSETUP_PROVISION_ONLINE_CALLER</b> in which case the locally running operating system directory is allowed. 

This path could
                     be a UNC path on a remote server.

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
<dt><b>ERROR_ELEVATION_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation requires elevation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>pProvisionBinData</i>, <i>cbProvisionBinDataSize</i>, or <i>lpWindowsPath</i> parameters are <b>NULL</b>.  This error is also returned if the buffer pointed to by the <i>pProvisionBinData</i> parameter does not contain valid data in the blob for the domain, machine account name, or machine account password. This error is also returned if the string pointed to <i>lpWindowsPath</i> parameter does not specific the path to a Windows operating system image.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the specified server does not support this operation. For example, if the <i>lpWindowsPath</i> parameter references a Windows installation configured as a domain controller.

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
</table>

## -remarks

The <b>NetRequestOfflineDomainJoin</b> function is supported on Windows 7 for offline domain join operations.  

The 
				<b>NetRequestOfflineDomainJoin</b> function is used locally on a machine to modify a Windows operating system image mounted on a volume. The registry is loaded for the image and provisioning blob data is written where it can be retrieved during the completion phase of an offline domain join operation. The offline domain join scenario uses these functions as follows:<ul>
<li>
<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>  is a provisioning function that is first called to perform the network operations necessary to create and configure the computer object in Active Directory. The output from the <b>NetProvisionComputerAccount</b> is an opaque binary blob of serialized metadata used for the next step.</li>
<li><b>NetRequestOfflineDomainJoin</b> , an image initialization function,   is then called to inject the output from the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> provisioning function into a Windows operating system image to be used during installation.  Changes to Windows initialization code will detect this saved state and affect the local only portion of domain join. </li>
</ul>


The <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function will create or reuse the machine account in the domain, collect all necessary metadata and return it in an opaque versioned binary blob or as text for embedding in an unattended setup answer file. The opaque binary blob can be consumed by the offline domain join request operation supplying all the necessary input to complete the domain join during first boot without any network operations (local state updates only). Note that the blob contains machine account password material essentially in the clear. The design makes no provisions for securing this data.  This problem exists today with unattended setup answer files which can carry a number of secrets including domain user passwords. The caller must secure the blob and the unattended setup files. Solutions to this problem are varied. As an example, a pre-exchanged key could be used to encrypt a session between the consumer and provisioning entity enabling a secure transfer of the opaque blob .


The opaque blob returned in the  <i>pProvisionBinData</i> parameter by the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a> function is versioned to allow interoperability and serviceability scenarios between different versions of Windows (joining client, provisioning machine, and domain controller). The offline join scenario currently does not limit the lifetime of the blob returned by the <b>NetProvisionComputerAccount</b> function.   

For more information on offline domain join operations, see the <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd392267(v=ws.10)">Offline Domain Join Step-by-Step Guide</a>
