---
UID: NF:certenroll.IAlternativeName.get_StrValue
title: IAlternativeName::get_StrValue
author: windows-sdk-content
description: Retrieves a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered object identifier (OID), or a user principal name (UPN).
old-location: security\ialternativename_strvalue_property.htm
tech.root: seccertenroll
ms.assetid: 1d916450-4a4e-4f11-b95b-dbf9693b7cdd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IAlternativeName interface [Security],StrValue property, IAlternativeName.StrValue, IAlternativeName.get_StrValue, IAlternativeName::StrValue, IAlternativeName::get_StrValue, StrValue property [Security], StrValue property [Security],IAlternativeName interface, certenroll/IAlternativeName::StrValue, certenroll/IAlternativeName::get_StrValue, get_StrValue, security.ialternativename_strvalue_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IAlternativeName.StrValue
 - IAlternativeName.get_StrValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlternativeName::get_StrValue


## -description


The <b>StrValue</b> property retrieves a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), or a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN).

This property is read-only.


## -parameters


## -remarks



You can call this property to retrieve a string if you initialized the <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> object by calling the <a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a> method and specifying one of the following <a href="https://msdn.microsoft.com/79b675cc-c979-46ab-aee1-0031af2efd40">AlternativeNameType</a> values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a DNS name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered OID.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a UPN.</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>
 

 

