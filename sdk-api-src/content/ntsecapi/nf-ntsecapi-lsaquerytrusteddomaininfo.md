---
UID: NF:ntsecapi.LsaQueryTrustedDomainInfo
title: LsaQueryTrustedDomainInfo function
author: windows-sdk-content
description: The LsaQueryTrustedDomainInfo function retrieves information about a trusted domain.
old-location: security\lsaquerytrusteddomaininfo.htm
old-project: SecMgmt
ms.assetid: 62925515-a6f3-4b5f-bf97-edb968af19a3
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LsaQueryTrustedDomainInfo, LsaQueryTrustedDomainInfo function [Security], TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixOffsetInformation, _lsa_lsaquerytrusteddomaininfo, ntsecapi/LsaQueryTrustedDomainInfo, security.lsaquerytrusteddomaininfo
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LsaQueryTrustedDomainInfo
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LsaQueryTrustedDomainInfo function


## -description


The <b>LsaQueryTrustedDomainInfo</b> function retrieves information about a trusted domain.


## -parameters




### -param PolicyHandle [in]

A handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object of a domain controller that has a trust relationship with the domain identified by the <i>TrustedDomainSid</i> parameter. The handle must have the POLICY_VIEW_LOCAL_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain to query.


### -param InformationClass [in]

Specifies one of the following values from the 
<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information being requested. 




					

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
Retrieves the name of the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="https://msdn.microsoft.com/9bc1301b-1d09-4cd2-8590-e7756ee4792d">TRUSTED_DOMAIN_NAME_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixOffsetInformation"></a><a id="trustedposixoffsetinformation"></a><a id="TRUSTEDPOSIXOFFSETINFORMATION"></a><dl>
<dt><b>TrustedPosixOffsetInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the value used to generate Posix user and group identifiers for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the password for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="https://msdn.microsoft.com/2c3aca10-8efd-4278-8127-2d31db776c0e">TRUSTED_PASSWORD_INFO</a> structure. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_GET_PRIVATE_INFORMATION access right.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Retrieves extended information for the trusted domain. The <i>Buffer</i> parameter receives a pointer to a 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainInformationBasic"></a><a id="trusteddomaininformationbasic"></a><a id="TRUSTEDDOMAININFORMATIONBASIC"></a><dl>
<dt><b>TrustedDomainInformationBasic</b></dt>
</dl>
</td>
<td width="60%">
This value is not supported.
							

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainFullInformation"></a><a id="trusteddomainfullinformation"></a><a id="TRUSTEDDOMAINFULLINFORMATION"></a><dl>
<dt><b>TrustedDomainFullInformation</b></dt>
</dl>
</td>
<td width="60%">
Retrieves complete information for the trusted domain. This information includes the Posix offset information, authentication information, and the extended information returned for the TrustedDomainInformationEx value. The <i>Buffer</i> parameter receives a pointer to a 
<a href="https://msdn.microsoft.com/b7abfe1e-d9e6-4583-a738-c16190ffd44d">TRUSTED_DOMAIN_FULL_INFORMATION</a> structure.

</td>
</tr>
</table>
 


### -param Buffer [out]

A pointer to a buffer that receives a pointer to a structure that contains the requested information. The type of structure depends on the value of the <i>InformationClass</i> parameter. 




When you have finished using the information, free the returned pointer by passing it to 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value that indicates the error. For more information, see 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/0e38ac5f-40db-405d-9394-b6bcb7c652b5">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a>



<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/f66abe33-d8c8-45b8-9b94-d6890d786aaa">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="https://msdn.microsoft.com/ef4d1d1d-9b1b-4d67-80b8-2b548ec31a87">POLICY_MODIFICATION_INFO</a>



<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

