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

# AlternativeNameType enumeration


## -description


The <b>AlternativeNameType</b> enumeration  specifies the alternative name types that can be specified when initializing an <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> object. Alternative names are used to create a version 3 <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> <b>AlternativeNames</b> extension. You can create this extension by using the <a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a> interface.


## -enum-fields




### -field XCN_CERT_ALT_NAME_UNKNOWN

The name type is not identified.


### -field XCN_CERT_ALT_NAME_OTHER_NAME

The name consists of an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a byte array that contains the name value.


### -field XCN_CERT_ALT_NAME_RFC822_NAME

The name is an email address such as  <i>someone@example.com</i>.


### -field XCN_CERT_ALT_NAME_DNS_NAME

The name is a Domain Name System (DNS) name such as <i>MyDomain.Microsoft.com</i>. The format of a DNS name is <i>Host.Entity.Domain</i>. For more information about DNS, see RFC 1034 (Domain Names—Concepts and Facilities), and RFC 1035 (Domain Names—Implementation and Specification).


### -field XCN_CERT_ALT_NAME_X400_ADDRESS


### -field XCN_CERT_ALT_NAME_DIRECTORY_NAME

The name is an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> directory name such as <i>CN=administrators,CN=users,DC=nttest,DC=microsoft,DC=com</i>.


### -field XCN_CERT_ALT_NAME_EDI_PARTY_NAME


### -field XCN_CERT_ALT_NAME_URL

The name is a URL such as <i>http://www.adatum.com/</i>.


### -field XCN_CERT_ALT_NAME_IP_ADDRESS

The name is an Internet Protocol (IP) address in dotted decimal format <i>123.456.789.123</i>.


### -field XCN_CERT_ALT_NAME_REGISTERED_ID

The name is an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) registered with the International Standards Organization (ISO).


### -field XCN_CERT_ALT_NAME_GUID

The name is a Directory Service Agent GUID. The GUID identifies a server to the Active Directory replication system as a domain controller.


### -field XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME

The name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN). A UPN is a user logon name in email address format. That is, a UPN consists of a shorthand name for a user account followed by the DNS name of the Active Directory tree in which the user object resides. It has the form <i>UserName@DNS_suffix</i>. An example is <i>UserName@Microsoft.com</i> where Microsoft.com is the  DNS suffix and <i>UserName</i> is a placeholder for a shorthand name assigned by Microsoft to a user account.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>



<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 

