---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# LsaQueryDomainInformationPolicy function


## -description


The <b>LsaQueryDomainInformationPolicy</b> function retrieves domain information from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>
    object.


## -parameters




### -param PolicyHandle [in]

A handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object for the system.


### -param InformationClass [in]


<a href="https://msdn.microsoft.com/b208c479-a262-4120-824f-677ead1ef61a">POLICY_DOMAIN_INFORMATION_CLASS</a> enumeration that specifies the information to be returned from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>
    object. The following table shows the possible values.

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



The POLICY_VIEW_LOCAL_INFORMATION access type is required to retrieve domain information from the  <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a>
    object. For more information, see <a href="https://msdn.microsoft.com/592dea65-9da1-4e49-82e4-8e08c451e026">Policy Object Access Rights</a>.



