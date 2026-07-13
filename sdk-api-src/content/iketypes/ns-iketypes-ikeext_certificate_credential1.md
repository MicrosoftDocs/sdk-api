---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CREDENTIAL1_
title: IKEEXT_CERTIFICATE_CREDENTIAL1 (iketypes.h)
description: Is used to store credential information specific to certificate authentication. (IKEEXT_CERTIFICATE_CREDENTIAL1)
helpviewer_keywords: ["IKEEXT_CERTIFICATE_CREDENTIAL1","IKEEXT_CERTIFICATE_CREDENTIAL1 structure [Filtering]","IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT","fwp.ikeext_certificate_credential1","iketypes/IKEEXT_CERTIFICATE_CREDENTIAL1"]
old-location: fwp\ikeext_certificate_credential1.htm
tech.root: fwp
ms.assetid: 78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERTIFICATE_CREDENTIAL1, IKEEXT_CERTIFICATE_CREDENTIAL1 structure [Filtering], IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT, fwp.ikeext_certificate_credential1, iketypes/IKEEXT_CERTIFICATE_CREDENTIAL1
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CERTIFICATE_CREDENTIAL1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERTIFICATE_CREDENTIAL1_
 - iketypes/IKEEXT_CERTIFICATE_CREDENTIAL1_
 - IKEEXT_CERTIFICATE_CREDENTIAL1
 - iketypes/IKEEXT_CERTIFICATE_CREDENTIAL1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CERTIFICATE_CREDENTIAL1
---

# IKEEXT_CERTIFICATE_CREDENTIAL1 structure


## -description

The [IKEEXT_CERTIFICATE_CREDENTIAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential0) is available.</div>
<div> </div>

## -struct-fields

### -field subjectName

Encoded subject name of the certificate used for authentication. Use <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> to convert the encoded name to string.

See [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) for more information.

### -field certHash

SHA thumbprint of the certificate.

See [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) for more information.

### -field flags

Possible values:

<a id="IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT"></a>
<a id="ikeext_cert_credential_flag_nap_cert"></a>


#### IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT

### -field certificate

The encoded certificate. Use <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a> to create a certificate context from the encoded certificate.

See [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob) for more information.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
