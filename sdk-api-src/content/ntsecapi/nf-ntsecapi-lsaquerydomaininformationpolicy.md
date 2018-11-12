---
UID: NF:ntsecapi.LsaQueryDomainInformationPolicy
title: LsaQueryDomainInformationPolicy function
author: windows-sdk-content
description: Retrieves domain information from the Policyobject.
old-location: security\lsaquerydomaininformationpolicy.htm
tech.root: secauthn
ms.assetid: 39a511d7-46fc-4d12-ba43-771f6db2a33b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: LsaQueryDomainInformationPolicy, LsaQueryDomainInformationPolicy function [Security], PolicyDomainEfsInformation, PolicyDomainKerberosTicketInformation, ntsecapi/LsaQueryDomainInformationPolicy, security.lsaquerydomaininformationpolicy, security.lsaquerydomaininformationpolicy_
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
 - LsaQueryDomainInformationPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaQueryDomainInformationPolicy function


## -description


The <b>LsaQueryDomainInformationPolicy</b> function retrieves domain information from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>object.


## -parameters




### -param PolicyHandle [in]

A handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object for the system.


### -param InformationClass [in]


<a href="https://msdn.microsoft.com/b208c479-a262-4120-824f-677ead1ef61a">POLICY_DOMAIN_INFORMATION_CLASS</a> enumeration that specifies the information to be returned from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>object. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyDomainEfsInformation"></a><a id="policydomainefsinformation"></a><a id="POLICYDOMAINEFSINFORMATION"></a><dl>
<dt><b>PolicyDomainEfsInformation</b></dt>
</dl>
</td>
<td width="60%">
The information is for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">Encrypting File System</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyDomainKerberosTicketInformation"></a><a id="policydomainkerberosticketinformation"></a><a id="POLICYDOMAINKERBEROSTICKETINFORMATION"></a><dl>
<dt><b>PolicyDomainKerberosTicketInformation</b></dt>
</dl>
</td>
<td width="60%">
The information is for a Kerberos ticket.

</td>
</tr>
</table>
 


### -param Buffer [out]

Pointer to a buffer that receives the requested information.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the <a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INTERNAL_DB_CORRUPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The policy database is 
            corrupt.  The returned policy information is  not valid for
            the given class.

</td>
</tr>
</table>
 




## -remarks



The POLICY_VIEW_LOCAL_INFORMATION access type is required to retrieve domain information from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>object. For more information, see <a href="https://msdn.microsoft.com/592dea65-9da1-4e49-82e4-8e08c451e026">Policy Object Access Rights</a>.



