---
UID: NF:ntsecapi.LsaSetTrustedDomainInformation
title: LsaSetTrustedDomainInformation function
author: windows-sdk-content
description: The LsaSetTrustedDomainInformation function modifies a Policy object's information about a trusted domain.
old-location: security\lsasettrusteddomaininformation.htm
tech.root: SecMgmt
ms.assetid: a7b89ea7-af92-46ba-ac73-2fba1cc27680
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LsaSetTrustedDomainInformation, LsaSetTrustedDomainInformation function [Security], TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _lsa_lsasettrusteddomaininformation, ntsecapi/LsaSetTrustedDomainInformation, security.lsasettrusteddomaininformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LsaSetTrustedDomainInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LsaSetTrustedDomainInformation
: 
---

# LsaSetTrustedDomainInformation function


## -description


The <b>LsaSetTrustedDomainInformation</b> function modifies a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object's information about a trusted domain.


## -parameters




### -param PolicyHandle [in]

A handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object of a domain controller. The required user rights for this handle depend on the value of the <i>InformationClass</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain whose information is modified. If the <i>InformationClass</i> parameter is set to TrustedDomainNameInformation, this parameter must point to the SID of the domain to add to the list of trusted domains.


### -param InformationClass [in]

Specifies one of the following values from the 
<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information being set. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainNameInformation"></a><a id="trusteddomainnameinformation"></a><a id="TRUSTEDDOMAINNAMEINFORMATION"></a><dl>
<dt><b>TrustedDomainNameInformation</b></dt>
</dl>
</td>
<td width="60%">
If the specified domain is not in the list of trusted domains, the 
<b>LsaSetTrustedDomainInformation</b> function adds it. The <i>TrustedDomainSid</i> parameter must be the SID of the domain to add. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/9bc1301b-1d09-4cd2-8590-e7756ee4792d">TRUSTED_DOMAIN_NAME_INFO</a> structure containing the name of the domain to add.  




If the specified domain is already in the list of trusted domains, the function fails.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixOffsetInformation"></a><a id="trustedposixoffsetinformation"></a><a id="TRUSTEDPOSIXOFFSETINFORMATION"></a><dl>
<dt><b>TrustedPosixOffsetInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the value used to generate Posix user and group identifiers. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the password for the trusted domain. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/2c3aca10-8efd-4278-8127-2d31db776c0e">TRUSTED_PASSWORD_INFO</a> structure containing the old and new passwords for the specified domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_CREATE_SECRET access right. The old password string can be <b>NULL</b>.

</td>
</tr>
</table>
 


### -param Buffer [in]

Pointer to a structure containing the information to set. The type of structure depends on the value of the <i>InformationClass</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/4a7afa28-1786-4a58-a955-d2d8b12e62e4">LsaDeleteTrustedDomain</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/9bc1301b-1d09-4cd2-8590-e7756ee4792d">TRUSTED_DOMAIN_NAME_INFO</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/2c3aca10-8efd-4278-8127-2d31db776c0e">TRUSTED_PASSWORD_INFO</a>



<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a>
 

 

