---
UID: NF:ntsecapi.LsaQueryTrustedDomainInfoByName
title: LsaQueryTrustedDomainInfoByName function
author: windows-sdk-content
description: The LsaQueryTrustedDomainInfoByName function returns information about a trusted domain.
old-location: security\lsaquerytrusteddomaininfobyname.htm
tech.root: secmgmt
ms.assetid: d33d6cee-bd8b-49f4-8e65-07cdc65bec7c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: LsaQueryTrustedDomainInfoByName, LsaQueryTrustedDomainInfoByName function [Security], TrustedDomainFullInformation, TrustedDomainInformationBasic, TrustedDomainInformationEx, TrustedDomainNameInformation, TrustedPasswordInformation, TrustedPosixInformation, _lsa_lsaquerytrusteddomaininfobyname, ntsecapi/LsaQueryTrustedDomainInfoByName, security.lsaquerytrusteddomaininfobyname
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
 - LsaQueryTrustedDomainInfoByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaQueryTrustedDomainInfoByName function


## -description


The <b>LsaQueryTrustedDomainInfoByName</b> function returns information about a trusted domain.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. This handle must have the POLICY_VIEW_LOCAL_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainName [in]

String that contains the name of the trusted domain. This can either be the domain name or the flat name.


### -param InformationClass [in]

Specifies the type of information to retrieve. This parameter can be one of the following values.

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
Name of the trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPosixInformation"></a><a id="trustedposixinformation"></a><a id="TRUSTEDPOSIXINFORMATION"></a><dl>
<dt><b>TrustedPosixInformation</b></dt>
</dl>
</td>
<td width="60%">
Posix offset of the trusted domain.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedPasswordInformation"></a><a id="trustedpasswordinformation"></a><a id="TRUSTEDPASSWORDINFORMATION"></a><dl>
<dt><b>TrustedPasswordInformation</b></dt>
</dl>
</td>
<td width="60%">
Returns the password on the outbound side of the trust.

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
<td width="40%"><a id="TrustedDomainInformationEx"></a><a id="trusteddomaininformationex"></a><a id="TRUSTEDDOMAININFORMATIONEX"></a><dl>
<dt><b>TrustedDomainInformationEx</b></dt>
</dl>
</td>
<td width="60%">
Extended trust information, including the basic information and DNS domain name, and attributes about the trust.

</td>
</tr>
<tr>
<td width="40%"><a id="TrustedDomainFullInformation"></a><a id="trusteddomainfullinformation"></a><a id="TRUSTEDDOMAINFULLINFORMATION"></a><dl>
<dt><b>TrustedDomainFullInformation</b></dt>
</dl>
</td>
<td width="60%">
Full information, including the Posix offset and the authentication information.

</td>
</tr>
</table>
 


### -param Buffer [out]

Receives a pointer to the returned buffer that contains the requested information. The format and content of this buffer depend on the information class. For example, if <i>InformationClass</i> is set to TrustedDomainInformationEx, <i>Buffer</i> receives a pointer to a 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure. For more information, see 
<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>. 




When you have finished using the buffer, free it by calling the <a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a> function.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> value, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have the appropriate access to complete the operation. For a list of the required access types, see the description of the <i>InformationClass</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_
RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Insufficient system resources, such as memory, to complete the call.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> value to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/263e1025-1010-463d-8bc7-cdf916ce9872">LsaSetTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

