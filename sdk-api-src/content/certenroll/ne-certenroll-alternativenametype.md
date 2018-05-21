---
UID: NE:certenroll.AlternativeNameType
title: AlternativeNameType
author: windows-driver-content
description: Specifies the alternative name types that can be specified when initializing an IAlternativeName object.
old-location: security\alternativenametype_enum.htm
old-project: SecCertEnroll
ms.assetid: 79b675cc-c979-46ab-aee1-0031af2efd40
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: AlternativeNameType, AlternativeNameType enumeration [Security], XCN_CERT_ALT_NAME_DIRECTORY_NAME, XCN_CERT_ALT_NAME_DNS_NAME, XCN_CERT_ALT_NAME_GUID, XCN_CERT_ALT_NAME_IP_ADDRESS, XCN_CERT_ALT_NAME_OTHER_NAME, XCN_CERT_ALT_NAME_REGISTERED_ID, XCN_CERT_ALT_NAME_RFC822_NAME, XCN_CERT_ALT_NAME_UNKNOWN, XCN_CERT_ALT_NAME_URL, XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, certenroll/AlternativeNameType, certenroll/XCN_CERT_ALT_NAME_DIRECTORY_NAME, certenroll/XCN_CERT_ALT_NAME_DNS_NAME, certenroll/XCN_CERT_ALT_NAME_GUID, certenroll/XCN_CERT_ALT_NAME_IP_ADDRESS, certenroll/XCN_CERT_ALT_NAME_OTHER_NAME, certenroll/XCN_CERT_ALT_NAME_REGISTERED_ID, certenroll/XCN_CERT_ALT_NAME_RFC822_NAME, certenroll/XCN_CERT_ALT_NAME_UNKNOWN, certenroll/XCN_CERT_ALT_NAME_URL, certenroll/XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, security.alternativenametype_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: AlternativeNameType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	AlternativeNameType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
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
 

 

