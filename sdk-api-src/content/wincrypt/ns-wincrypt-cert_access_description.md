---
UID: NS:wincrypt._CERT_ACCESS_DESCRIPTION
title: CERT_ACCESS_DESCRIPTION (wincrypt.h)
description: The CERT_ACCESS_DESCRIPTION structure is a member of a CERT_AUTHORITY_INFO_ACCESS structure.
helpviewer_keywords: ["*PCERT_ACCESS_DESCRIPTION","CERT_ACCESS_DESCRIPTION","CERT_ACCESS_DESCRIPTION structure [Security]","PCERT_ACCESS_DESCRIPTION","PCERT_ACCESS_DESCRIPTION structure pointer [Security]","_crypto2_cert_access_description","security.cert_access_description","wincrypt/CERT_ACCESS_DESCRIPTION","wincrypt/PCERT_ACCESS_DESCRIPTION"]
old-location: security\cert_access_description.htm
tech.root: security
ms.assetid: 5e1e5b04-92af-45b1-acfd-17852c245d89
ms.date: 12/05/2018
ms.keywords: '*PCERT_ACCESS_DESCRIPTION, CERT_ACCESS_DESCRIPTION, CERT_ACCESS_DESCRIPTION structure [Security], PCERT_ACCESS_DESCRIPTION, PCERT_ACCESS_DESCRIPTION structure pointer [Security], _crypto2_cert_access_description, security.cert_access_description, wincrypt/CERT_ACCESS_DESCRIPTION, wincrypt/PCERT_ACCESS_DESCRIPTION'
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
req.typenames: CERT_ACCESS_DESCRIPTION, *PCERT_ACCESS_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_ACCESS_DESCRIPTION
 - wincrypt/_CERT_ACCESS_DESCRIPTION
 - PCERT_ACCESS_DESCRIPTION
 - wincrypt/PCERT_ACCESS_DESCRIPTION
 - CERT_ACCESS_DESCRIPTION
 - wincrypt/CERT_ACCESS_DESCRIPTION
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
 - CERT_ACCESS_DESCRIPTION
---

# CERT_ACCESS_DESCRIPTION structure


## -description

The <b>CERT_ACCESS_DESCRIPTION</b> structure is a member of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_info_access">CERT_AUTHORITY_INFO_ACCESS</a> structure. It contains one instance of information about how to access information and services for either the subject or the issuer of a certificate that contains either the subject information access or the authority information access extension, respectively. For more information about these certificate extensions, see <a href="https://www.ietf.org/rfc/rfc3280.txt">RFC 3280</a>.

## -struct-fields

### -field pszAccessMethod

Specifies the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the method of access.

The following are currently defined PKIX Access Method OIDs:

<ul>
<li>szOID_PKIX_CA_ISSUERS</li>
<li>szOID_PKIX_CA_REPOSITORY</li>
<li>szOID_PKIX_OCSP</li>
<li>szOID_PKIX_TIME_STAMPING</li>
</ul>
The default provider does not support the szOID_PKIX_TIME_STAMPING method.

### -field AccessLocation

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure that describes the online status server and the access protocol to obtain current certificate status information for the certificate containing the extension. 




For the szOID_PKIX_OCSP access method, <b>AccessLocation</b> describes the online status server and the access protocol needed to obtain status information about the certificate containing this extension.

For the szOID_PKIX_CA_ISSUERS access method, <b>AccessLocation</b> obtains information on the CAs that issued certificates superior to the CA that issued the certificate containing this extension. The CA issuer's description is intended to aid certificate users in the selection of a certification path that terminates at a point trusted by the certificate user.

For the szOID_PKIX_CA_REPOSITORY method, <b>AccessLocation</b> specifies either the URI, directory name, or email address of the certificate and <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) repository for a  subject that is a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_info_access">CERT_AUTHORITY_INFO_ACCESS</a>



<a href="https://www.ietf.org/rfc/rfc3280.txt">RFC 3280</a>