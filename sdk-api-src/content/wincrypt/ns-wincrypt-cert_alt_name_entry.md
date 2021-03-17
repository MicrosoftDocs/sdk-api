---
UID: NS:wincrypt._CERT_ALT_NAME_ENTRY
title: CERT_ALT_NAME_ENTRY (wincrypt.h)
description: Contains an alternative name in one of a variety of name forms.
helpviewer_keywords: ["*PCERT_ALT_NAME_ENTRY","CERT_ALT_NAME_ENTRY","CERT_ALT_NAME_ENTRY structure [Security]","PCERT_ALT_NAME_ENTRY","PCERT_ALT_NAME_ENTRY structure pointer [Security]","_crypto2_cert_alt_name_entry","security.cert_alt_name_entry","wincrypt/CERT_ALT_NAME_ENTRY","wincrypt/PCERT_ALT_NAME_ENTRY"]
old-location: security\cert_alt_name_entry.htm
tech.root: security
ms.assetid: 1353ef56-cae7-43f2-a31f-2bb3b502450e
ms.date: 12/05/2018
ms.keywords: '*PCERT_ALT_NAME_ENTRY, CERT_ALT_NAME_ENTRY, CERT_ALT_NAME_ENTRY structure [Security], PCERT_ALT_NAME_ENTRY, PCERT_ALT_NAME_ENTRY structure pointer [Security], _crypto2_cert_alt_name_entry, security.cert_alt_name_entry, wincrypt/CERT_ALT_NAME_ENTRY, wincrypt/PCERT_ALT_NAME_ENTRY'
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
targetos: Windows
req.typenames: CERT_ALT_NAME_ENTRY, *PCERT_ALT_NAME_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_ALT_NAME_ENTRY
 - wincrypt/_CERT_ALT_NAME_ENTRY
 - PCERT_ALT_NAME_ENTRY
 - wincrypt/PCERT_ALT_NAME_ENTRY
 - CERT_ALT_NAME_ENTRY
 - wincrypt/CERT_ALT_NAME_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_ALT_NAME_ENTRY
---

# CERT_ALT_NAME_ENTRY structure


## -description

The <b>CERT_ALT_NAME_ENTRY</b> structure contains an alternative name in one of a variety of name forms. These names are bound by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) to a certificate's public key.

A  structure can be <b>CERT_ALT_NAME_ENTRY</b> member of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure.

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

A pointer to a <b>CERT_OTHER_NAME</b> structure, which includes an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> containing the name.

### -field DUMMYUNIONNAME.pwszRfc822Name

Email address as a Unicode string.

### -field DUMMYUNIONNAME.pwszDNSName

DNS name as an IA5 string.

### -field DUMMYUNIONNAME.DirectoryName

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> structure that contains a directory name.

### -field DUMMYUNIONNAME.pwszURL

URL as a IA5 string.

### -field DUMMYUNIONNAME.IPAddress

Octet string that is an Internet Protocol address defined in accordance with Internet <a href="https://www.ietf.org/rfc/rfc791.txt">RFC 791</a>.

### -field DUMMYUNIONNAME.pszRegisteredID

Object identifier (OID) of any registered object.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>