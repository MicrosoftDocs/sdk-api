---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CRITERIA0_
title: IKEEXT_CERTIFICATE_CRITERIA0 (iketypes.h)
description: Contains a set of criteria to applied to an authentication method.
helpviewer_keywords: ["IKEEXT_CERTIFICATE_CRITERIA0","IKEEXT_CERTIFICATE_CRITERIA0 structure [Filtering]","fwp.ikeext_certificate_criteria0","iketypes/IKEEXT_CERTIFICATE_CRITERIA0"]
old-location: fwp\ikeext_certificate_criteria0.htm
tech.root: fwp
ms.assetid: dbcb0e25-fdde-44d9-bfad-b3605f563773
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERTIFICATE_CRITERIA0, IKEEXT_CERTIFICATE_CRITERIA0 structure [Filtering], fwp.ikeext_certificate_criteria0, iketypes/IKEEXT_CERTIFICATE_CRITERIA0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEEXT_CERTIFICATE_CRITERIA0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERTIFICATE_CRITERIA0_
 - iketypes/IKEEXT_CERTIFICATE_CRITERIA0_
 - IKEEXT_CERTIFICATE_CRITERIA0
 - iketypes/IKEEXT_CERTIFICATE_CRITERIA0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_CERTIFICATE_CRITERIA0
---

# IKEEXT_CERTIFICATE_CRITERIA0 structure


## -description

The <b>IKEEXT_CERTIFICATE_CRITERIA0</b> structure contains a set of criteria to applied to an authentication method.

## -struct-fields

### -field certData

Type: [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)</b>

X509/ASN.1 encoded name of the root certificate. Should be empty when
   specifying Enterprise or trusted root store config.

### -field certHash

Type: [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)</b>

  16-character hexadecimal string that represents the ID, thumbprint or HASH of the end certificate.

### -field eku

Type: [IKEEXT_CERT_EKUS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_ekus0)*</b>

The specific extended key usage (EKU) object identifiers (OIDs) selected for the criteria on the end certificate.

### -field name

Type: [IKEEXT_CERT_NAME0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_name0)*</b>

The name/subject selected for the criteria on the end certificate.

### -field flags

Type: <b>UINT32</b>

Reserved for system use.

## -remarks

The <b>certData</b> member refers to the encoded name of the root certificate, while the <b>certHash</b>, <b>eku</b>, and <b>name</b> members refer to criteria on the end certificate.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[IKEEXT_CERT_EKUS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_ekus0)



[IKEEXT_CERT_NAME0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cert_name0)