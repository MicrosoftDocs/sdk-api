---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CREDENTIAL0_
title: IKEEXT_CERTIFICATE_CREDENTIAL0 (iketypes.h)
description: Is used to store credential information specific to certificate authentication.
old-location: fwp\ikeext_certificate_credential0.htm
tech.root: fwp
ms.assetid: 926a7e74-a225-4234-8be0-c8731840756a
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERTIFICATE_CREDENTIAL0, IKEEXT_CERTIFICATE_CREDENTIAL0 structure [Filtering], IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT, fwp.ikeext_certificate_credential0, iketypes/IKEEXT_CERTIFICATE_CREDENTIAL0
f1_keywords:
- iketypes/IKEEXT_CERTIFICATE_CREDENTIAL0
dev_langs:
- c++
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Iketypes.h
api_name:
- IKEEXT_CERTIFICATE_CREDENTIAL0
targetos: Windows
req.typenames: IKEEXT_CERTIFICATE_CREDENTIAL0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_CERTIFICATE_CREDENTIAL0 structure


## -description


The <b>IKEEXT_CERTIFICATE_CREDENTIAL0</b> structure is used to store credential information specific to certificate authentication.
[IKEEXT_CERTIFICATE_CREDENTIAL1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_certificate_credential1)a> is available.</div><div> </div>

## -struct-fields




### -field subjectName

Encoded subject name of the certificate used for authentication.

See [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> for more information.


### -field certHash

SHA thumbprint of the certificate.

See [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> for more information.


### -field flags

Possible values:

<a id="IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT"></a>
<a id="ikeext_cert_credential_flag_nap_cert"></a>


#### IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

