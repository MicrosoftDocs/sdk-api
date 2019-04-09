---
UID: NS:lmjoin._NETSETUP_PROVISIONING_PARAMS
title: NETSETUP_PROVISIONING_PARAMS (lmjoin.h)
author: windows-sdk-content
description: The NETSETUP_PROVISIONING_PARAMS structure contains information that is used when creating a provisioning package using the NetCreateProvisionPackage function.
old-location: netmgmt\netsetup_provisioning_params.htm
tech.root: NetMgmt
ms.assetid: E965804F-145A-4D8F-BB8E-466580AC65DA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PNETSETUP_PROVISIONING_PARAMS, NETSETUP_PROVISIONING_PARAMS, NETSETUP_PROVISIONING_PARAMS structure [Network Management], NETSETUP_PROVISIONING_PARAMS_CURRENT_VERSION, NETSETUP_PROVISION_DOWNLEVEL_PRIV_SUPPORT, NETSETUP_PROVISION_REUSE_ACCOUNT, NETSETUP_PROVISION_ROOT_CA_CERTS, NETSETUP_PROVISION_SKIP_ACCOUNT_SEARCH, NETSETUP_PROVISION_USE_DEFAULT_PASSWORD, PNETSETUP_PROVISIONING_PARAMS, PNETSETUP_PROVISIONING_PARAMS structure pointer [Network Management], lmjoin/NETSETUP_PROVISIONING_PARAMS, lmjoin/PNETSETUP_PROVISIONING_PARAMS, netmgmt.netsetup_provisioning_params"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmjoin.h
api_name:
 - NETSETUP_PROVISIONING_PARAMS
product: Windows
targetos: Windows
req.typenames: NETSETUP_PROVISIONING_PARAMS, *PNETSETUP_PROVISIONING_PARAMS
req.redist: 
---

# NETSETUP_PROVISIONING_PARAMS structure


## -description


The <b>NETSETUP_PROVISIONING_PARAMS</b> structure contains information that is used when creating a provisioning package using the  <a href="https://msdn.microsoft.com/6E2A5578-8308-41E2-B5E9-5E34E9E76C0B">NetCreateProvisionPackage</a> function.


## -struct-fields




### -field dwVersion

The version of Windows in the provisioning package. This parameter should use the following value defined in the <i>Lmjoin.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSETUP_PROVISIONING_PARAMS_CURRENT_VERSION"></a><a id="netsetup_provisioning_params_current_version"></a><dl>
<dt><b>NETSETUP_PROVISIONING_PARAMS_CURRENT_VERSION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The version for this package is Windows Server 2012.

</td>
</tr>
</table>
 


### -field lpDomain

A pointer to a <b>NULL</b>-terminated character string that specifies the name of the domain where the computer account is created. 


 


### -field lpHostName

 


### -field lpMachineAccountOU

A optional pointer to a <b>NULL</b>-terminated character string that contains the RFC 1779 format name of the organizational unit (OU) where the computer account will be created. If you specify this parameter, the string must contain a full path, for example, OU=testOU,DC=domain,DC=Domain,DC=com. Otherwise, this parameter must be <b>NULL</b>.

If this parameter is <b>NULL</b>, the well known computer object container will be used as published in the domain.


### -field lpDcName

An optional pointer to a <b>NULL</b>-terminated character string that contains the name of the domain controller to target.


### -field dwProvisionOptions

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
This option retrieves all of the root Certificate Authority certificates on the local machine and adds them to the provisioning package.

<div class="alert"><b>Note</b>  This flag is only supported by the <a href="https://msdn.microsoft.com/6E2A5578-8308-41E2-B5E9-5E34E9E76C0B">NetCreateProvisioningPackage</a> function on Windows 8, Windows Server 2012, and later.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field aCertTemplateNames

A pointer to an array of <b>NULL</b>-terminated certificate template names. 


### -field cCertTemplateNames

When <b>aCertTemplateNames</b> is not <b>NULL</b>, this member provides an explicit count of the number of items in the array.


### -field aMachinePolicyNames

A pointer to an array of <b>NULL</b>-terminated  machine policy names.


### -field cMachinePolicyNames

When <b>aMachinePolicyNames</b> is not <b>NULL</b>, this member provides an explicit count of the number of items in the array.


### -field aMachinePolicyPaths

A pointer to an array of  character strings. Each array element is a NULL-terminated character string which specifies the full or partial path to a file in the Registry Policy File format. For more information on the Registry Policy File Format , see <a href="https://msdn.microsoft.com/f533d619-6a57-4376-b632-5c48248afc5d">Registry Policy File Format</a>


This path could
                     be a UNC path on a remote server.


### -field cMachinePolicyPaths

When <b>aMachinePolicyPaths</b> is not <b>NULL</b>, this member provides an explicit count of the number of items in the array.


### -field lpNetbiosName

 


### -field lpSiteName

 


### -field lpPrimaryDNSDomain

 




#### - lpMachineName

A pointer to a <b>NULL</b>-terminated character string that specifies the short name of the machine from which the computer account attribute sAMAccountName is derived by appending a '$'. This parameter must contain a valid DNS or NetBIOS machine name.


## -remarks



The <b>NETSETUP_PROVISIONING_PARAMS</b> structure  provides flags for the <a href="https://msdn.microsoft.com/6E2A5578-8308-41E2-B5E9-5E34E9E76C0B">NetCreateProvisioningPackage</a> function which is supported on Windows 8 and  Windows Server 2012 for offline join operations.

In addition to domain joins, the provisioning package can provide certificates and policies to the machine. The provisioning package can be used in four ways:<ul>
<li>Domain join</li>
<li>Domain join and installation of certificates</li>
<li>Domain join and installation of policies</li>
<li>Domain join and installation of certificates and policies</li>
</ul>


When certificates need to be added to the package, this structure provides the <b>aCertTemplateNames</b> member as an array of <b>NULL</b>-terminated certificate template names.  The  <b>aCertTemplateNames</b> member requires the <b>cCertTemplateNames</b> member to provide an explicit count of the number of items in the array.

There are two different ways to add policies. You can use one or both methods:<ul>
<li>Policy name—An array of <b>NULL</b>-terminated policy names is provided in the <b>aMachinePolicyNames</b> member. During runtime, the policy name is mapped to the policy name in AD and the GUID that represents the policy in the enterprise space is retrieved. The <b>aMachinePolicyNames</b> member requires the <b>cMachinePolicyNames</b> member to provide an explicit count of the number of items in the array.</li>
<li>Policy path—A pointer to an array of  <b>NULL</b>-terminated character strings provided in the <b>aMachinePolicyPaths</b> member which specify the path to a file in the Registry Policy File format. For more information on the Registry Policy File Format , see <a href="https://msdn.microsoft.com/f533d619-6a57-4376-b632-5c48248afc5d">Registry Policy File Format</a>. The policy path is a full or relative path to the policy file.</li>
</ul>





## -see-also




<b></b>



<a href="https://msdn.microsoft.com/6E2A5578-8308-41E2-B5E9-5E34E9E76C0B">NetCreateProvisionPackage</a>



<a href="https://msdn.microsoft.com/4efcb399-03af-4312-9f1d-6bc38f356cac">NetJoinDomain</a>



<a href="https://msdn.microsoft.com/4c854258-b84d-4ef3-a6da-ce0a9540ffd5">NetProvisionComputerAccount</a>



<a href="https://msdn.microsoft.com/1f7ddaa1-a349-49a6-856d-a2fde2f1dc3b">NetRenameMachineInDomain</a>



<a href="https://msdn.microsoft.com/f3f8fe00-d6f7-4d59-a4e7-6aef7f507e1a">NetRequestOfflineDomainJoin</a>



<a href="https://msdn.microsoft.com/107ED0F7-8DDD-4C18-8C34-3A67F771FA62">NetRequestProvisioningPackageInstall</a>



<a href="https://msdn.microsoft.com/cc755c22-1fd6-4787-999e-a43258287a05">NetUnjoinDomain</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

