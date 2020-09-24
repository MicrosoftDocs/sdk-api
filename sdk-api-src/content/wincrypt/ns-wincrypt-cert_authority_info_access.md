---
UID: NS:wincrypt._CERT_AUTHORITY_INFO_ACCESS
title: CERT_AUTHORITY_INFO_ACCESS (wincrypt.h)
description: Represents authority information access and subject information access certificate extensions and specifies how to access additional information and services for the subject or the issuer of a certificate.
helpviewer_keywords: ["*PCERT_AUTHORITY_INFO_ACCESS","*PCERT_SUBJECT_INFO_ACCESS","CERT_AUTHORITY_INFO_ACCESS","CERT_AUTHORITY_INFO_ACCESS structure [Security]","CERT_SUBJECT_INFO_ACCESS","CERT_SUBJECT_INFO_ACCESS structure [Security]","PCERT_AUTHORITY_INFO_ACCESS","PCERT_AUTHORITY_INFO_ACCESS structure pointer [Security]","PCERT_SUBJECT_INFO_ACCESS","PCERT_SUBJECT_INFO_ACCESS structure pointer [Security]","_crypto2_cert_authority_info_access","security.cert_authority_info_access","wincrypt/CERT_AUTHORITY_INFO_ACCESS","wincrypt/CERT_SUBJECT_INFO_ACCESS","wincrypt/PCERT_AUTHORITY_INFO_ACCESS","wincrypt/PCERT_SUBJECT_INFO_ACCESS"]
old-location: security\cert_authority_info_access.htm
tech.root: security
ms.assetid: 5f4abb15-3057-4d20-a319-550cec45d1f1
ms.date: 12/05/2018
ms.keywords: '*PCERT_AUTHORITY_INFO_ACCESS, *PCERT_SUBJECT_INFO_ACCESS, CERT_AUTHORITY_INFO_ACCESS, CERT_AUTHORITY_INFO_ACCESS structure [Security], CERT_SUBJECT_INFO_ACCESS, CERT_SUBJECT_INFO_ACCESS structure [Security], PCERT_AUTHORITY_INFO_ACCESS, PCERT_AUTHORITY_INFO_ACCESS structure pointer [Security], PCERT_SUBJECT_INFO_ACCESS, PCERT_SUBJECT_INFO_ACCESS structure pointer [Security], _crypto2_cert_authority_info_access, security.cert_authority_info_access, wincrypt/CERT_AUTHORITY_INFO_ACCESS, wincrypt/CERT_SUBJECT_INFO_ACCESS, wincrypt/PCERT_AUTHORITY_INFO_ACCESS, wincrypt/PCERT_SUBJECT_INFO_ACCESS'
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
req.typenames: CERT_AUTHORITY_INFO_ACCESS, *PCERT_AUTHORITY_INFO_ACCESS, CERT_SUBJECT_INFO_ACCESS, *PCERT_SUBJECT_INFO_ACCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_AUTHORITY_INFO_ACCESS
 - wincrypt/_CERT_AUTHORITY_INFO_ACCESS
 - PCERT_AUTHORITY_INFO_ACCESS
 - wincrypt/PCERT_AUTHORITY_INFO_ACCESS
 - CERT_AUTHORITY_INFO_ACCESS
 - wincrypt/CERT_AUTHORITY_INFO_ACCESS
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
 - CERT_AUTHORITY_INFO_ACCESS
---

# CERT_AUTHORITY_INFO_ACCESS structure


## -description

The <b>CERT_AUTHORITY_INFO_ACCESS</b> structure represents authority information access and subject information access certificate extensions and specifies how to access additional information and services for the subject or the issuer of a certificate.

## -struct-fields

### -field cAccDescr

The number of elements in the <b>rgAccDescr</b> array.

### -field rgAccDescr

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_access_description">CERT_ACCESS_DESCRIPTION</a> structures that describes the format and location of additional information about the certificate. Each <b>CERT_ACCESS_DESCRIPTION</b> structure has as its members a <b>pszAccessMethod</b> string that indicates an access method and a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure that indicates the location of the additional information.

## -remarks

The type of information represented by this structure depends on the access methods specified by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_access_description">CERT_ACCESS_DESCRIPTION</a> structures in the <i>rgAccDescr</i> array. For more information about access methods, the authority information access extension, and the subject information access extension, see <a href="https://www.ietf.org/rfc/rfc3280.txt">RFC 3280</a>.

The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> function creates an instance of this structure when decoding a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member and the <b>pszObjId</b> member of the <b>CERT_EXTENSION</b> structure is set to szOID_AUTHORITY_INFO_ACCESS or szOID_SUBJECT_INFO_ACCESS.

An instance of this structure can be used as input to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function to create an appropriate <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_access_description">CERT_ACCESS_DESCRIPTION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a>



<a href="https://www.ietf.org/rfc/rfc3280.txt">RFC 3280</a>