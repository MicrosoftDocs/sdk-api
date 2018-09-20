---
UID: NS:wincrypt._CERT_ALT_NAME_ENTRY
title: "_CERT_ALT_NAME_ENTRY"
author: windows-sdk-content
description: Contains an alternative name in one of a variety of name forms.
old-location: security\cert_alt_name_entry.htm
tech.root: seccrypto
ms.assetid: 1353ef56-cae7-43f2-a31f-2bb3b502450e
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PCERT_ALT_NAME_ENTRY, CERT_ALT_NAME_ENTRY, CERT_ALT_NAME_ENTRY structure [Security], PCERT_ALT_NAME_ENTRY, PCERT_ALT_NAME_ENTRY structure pointer [Security], _CERT_ALT_NAME_ENTRY, _crypto2_cert_alt_name_entry, security.cert_alt_name_entry, wincrypt/CERT_ALT_NAME_ENTRY, wincrypt/PCERT_ALT_NAME_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_ALT_NAME_ENTRY
product: Windows
targetos: Windows
req.typenames: CERT_ALT_NAME_ENTRY, *PCERT_ALT_NAME_ENTRY
req.redist: 
---

# _CERT_ALT_NAME_ENTRY structure


## -description


The <b>CERT_ALT_NAME_ENTRY</b> structure contains an alternative name in one of a variety of name forms. These names are bound by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) to a certificate's public key.

A  structure can be <b>CERT_ALT_NAME_ENTRY</b> member of a 
<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> structure.


## -struct-fields




### -field dwAltNameChoice

Indicates the <b>union</b> variant used for the alternative name.

This can be one of the following values:

<ul>
<li>CERT_ALT_NAME_OTHER_NAME</li>
<li>CERT_ALT_NAME_RFC822_NAME</li>
<li>CERT_ALT_NAME_DNS_NAME</li>
<li>CERT_ALT_NAME_DIRECTORY_NAME</li>
<li>CERT_ALT_NAME_URL</li>
<li>CERT_ALT_NAME_IP_ADDRESS</li>
<li>CERT_ALT_NAME_REGISTERED_ID</li>
</ul>

### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.pOtherName

A pointer to a <b>CERT_OTHER_NAME</b> structure, which includes an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> containing the name.


### -field DUMMYUNIONNAME.pwszRfc822Name

Email address as a Unicode string.


### -field DUMMYUNIONNAME.pwszDNSName

DNS name as an IA5 string.


### -field DUMMYUNIONNAME.DirectoryName

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> structure that contains a directory name.


### -field DUMMYUNIONNAME.pwszURL

URL as a IA5 string.


### -field DUMMYUNIONNAME.IPAddress

Octet string that is an Internet Protocol address defined in accordance with Internet <a href="http://go.microsoft.com/fwlink/p/?linkid=84067">RFC 791</a>.


### -field DUMMYUNIONNAME.pszRegisteredID

Object identifier (OID) of any registered object.


## -see-also




<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a>



<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

