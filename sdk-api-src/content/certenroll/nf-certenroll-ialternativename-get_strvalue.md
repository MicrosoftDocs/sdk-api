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


The <b>StrValue</b> property retrieves a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID), or a <a href="https://msdn.microsoft.com/en-us/library/ms721629(v=VS.85).aspx">user principal name</a> (UPN).

This property is read-only.


## -parameters


## -remarks



You can call this property to retrieve a string if you initialized the <a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a> object by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375024(v=VS.85).aspx">InitializeFromString</a> method and specifying one of the following <a href="https://msdn.microsoft.com/en-us/library/Aa374830(v=VS.85).aspx">AlternativeNameType</a> values.<table>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a>
 

 

