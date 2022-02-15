---
UID: NE:certenroll.AlternativeNameType
title: AlternativeNameType (certenroll.h)
description: Specifies the alternative name types that can be specified when initializing an IAlternativeName object.
helpviewer_keywords: ["AlternativeNameType","AlternativeNameType enumeration [Security]","XCN_CERT_ALT_NAME_DIRECTORY_NAME","XCN_CERT_ALT_NAME_DNS_NAME","XCN_CERT_ALT_NAME_GUID","XCN_CERT_ALT_NAME_IP_ADDRESS","XCN_CERT_ALT_NAME_OTHER_NAME","XCN_CERT_ALT_NAME_REGISTERED_ID","XCN_CERT_ALT_NAME_RFC822_NAME","XCN_CERT_ALT_NAME_UNKNOWN","XCN_CERT_ALT_NAME_URL","XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME","certenroll/AlternativeNameType","certenroll/XCN_CERT_ALT_NAME_DIRECTORY_NAME","certenroll/XCN_CERT_ALT_NAME_DNS_NAME","certenroll/XCN_CERT_ALT_NAME_GUID","certenroll/XCN_CERT_ALT_NAME_IP_ADDRESS","certenroll/XCN_CERT_ALT_NAME_OTHER_NAME","certenroll/XCN_CERT_ALT_NAME_REGISTERED_ID","certenroll/XCN_CERT_ALT_NAME_RFC822_NAME","certenroll/XCN_CERT_ALT_NAME_UNKNOWN","certenroll/XCN_CERT_ALT_NAME_URL","certenroll/XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME","security.alternativenametype_enum"]
old-location: security\alternativenametype_enum.htm
tech.root: security
ms.assetid: 79b675cc-c979-46ab-aee1-0031af2efd40
ms.date: 12/05/2018
ms.keywords: AlternativeNameType, AlternativeNameType enumeration [Security], XCN_CERT_ALT_NAME_DIRECTORY_NAME, XCN_CERT_ALT_NAME_DNS_NAME, XCN_CERT_ALT_NAME_GUID, XCN_CERT_ALT_NAME_IP_ADDRESS, XCN_CERT_ALT_NAME_OTHER_NAME, XCN_CERT_ALT_NAME_REGISTERED_ID, XCN_CERT_ALT_NAME_RFC822_NAME, XCN_CERT_ALT_NAME_UNKNOWN, XCN_CERT_ALT_NAME_URL, XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, certenroll/AlternativeNameType, certenroll/XCN_CERT_ALT_NAME_DIRECTORY_NAME, certenroll/XCN_CERT_ALT_NAME_DNS_NAME, certenroll/XCN_CERT_ALT_NAME_GUID, certenroll/XCN_CERT_ALT_NAME_IP_ADDRESS, certenroll/XCN_CERT_ALT_NAME_OTHER_NAME, certenroll/XCN_CERT_ALT_NAME_REGISTERED_ID, certenroll/XCN_CERT_ALT_NAME_RFC822_NAME, certenroll/XCN_CERT_ALT_NAME_UNKNOWN, certenroll/XCN_CERT_ALT_NAME_URL, certenroll/XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, security.alternativenametype_enum
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AlternativeNameType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AlternativeNameType
 - certenroll/AlternativeNameType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - AlternativeNameType
---

# AlternativeNameType enumeration


## -description

The <b>AlternativeNameType</b> enumeration  specifies the alternative name types that can be specified when initializing an <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> object. Alternative names are used to create a version 3 <a href="/windows/desktop/SecGloss/x-gly">X.509</a> <b>AlternativeNames</b> extension. You can create this extension by using the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a> interface.

## -enum-fields

### -field XCN_CERT_ALT_NAME_UNKNOWN:0

The name type is not identified.

### -field XCN_CERT_ALT_NAME_OTHER_NAME:1

The name consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a byte array that contains the name value.

### -field XCN_CERT_ALT_NAME_RFC822_NAME:2

The name is an email address such as  <i>someone@example.com</i>.

### -field XCN_CERT_ALT_NAME_DNS_NAME:3

The name is a Domain Name System (DNS) name such as <i>MyDomain.Microsoft.com</i>. The format of a DNS name is <i>Host.Entity.Domain</i>. For more information about DNS, see RFC 1034 (Domain Names—Concepts and Facilities), and RFC 1035 (Domain Names—Implementation and Specification).

### -field XCN_CERT_ALT_NAME_X400_ADDRESS:4

### -field XCN_CERT_ALT_NAME_DIRECTORY_NAME:5

The name is an <a href="/windows/desktop/SecGloss/x-gly">X.500</a> directory name such as <i>CN=administrators,CN=users,DC=nttest,DC=microsoft,DC=com</i>.

### -field XCN_CERT_ALT_NAME_EDI_PARTY_NAME:6

### -field XCN_CERT_ALT_NAME_URL:7

The name is a URL such as <i>http://www.adatum.com/</i>.

### -field XCN_CERT_ALT_NAME_IP_ADDRESS:8

The name is an Internet Protocol (IP) address in dotted decimal format <i>123.456.789.123</i>.

### -field XCN_CERT_ALT_NAME_REGISTERED_ID:9

The name is an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) registered with the International Standards Organization (ISO).

### -field XCN_CERT_ALT_NAME_GUID:10

The name is a Directory Service Agent GUID. The GUID identifies a server to the Active Directory replication system as a domain controller.

### -field XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME:11

The name is a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN). A UPN is a user logon name in email address format. That is, a UPN consists of a shorthand name for a user account followed by the DNS name of the Active Directory tree in which the user object resides. It has the form <i>UserName@DNS_suffix</i>. An example is <i>UserName@Microsoft.com</i> where Microsoft.com is the  DNS suffix and <i>UserName</i> is a placeholder for a shorthand name assigned by Microsoft to a user account.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>
