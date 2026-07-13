---
UID: NE:iketypes.IKEEXT_CERT_CRITERIA_NAME_TYPE_
title: IKEEXT_CERT_CRITERIA_NAME_TYPE (iketypes.h)
description: Specifies the type of NAME fields possible for a certificate selection &quot;subject&quot; criteria.
helpviewer_keywords: ["IKEEXT_CERT_CRITERIA_CN","IKEEXT_CERT_CRITERIA_DC","IKEEXT_CERT_CRITERIA_DNS","IKEEXT_CERT_CRITERIA_NAME_TYPE","IKEEXT_CERT_CRITERIA_NAME_TYPE enumeration [Filtering]","IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX","IKEEXT_CERT_CRITERIA_O","IKEEXT_CERT_CRITERIA_OU","IKEEXT_CERT_CRITERIA_RFC822","IKEEXT_CERT_CRITERIA_UPN","fwp.ikeext_cert_criteria_name_type","iketypes/IKEEXT_CERT_CRITERIA_CN","iketypes/IKEEXT_CERT_CRITERIA_DC","iketypes/IKEEXT_CERT_CRITERIA_DNS","iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE","iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX","iketypes/IKEEXT_CERT_CRITERIA_O","iketypes/IKEEXT_CERT_CRITERIA_OU","iketypes/IKEEXT_CERT_CRITERIA_RFC822","iketypes/IKEEXT_CERT_CRITERIA_UPN"]
old-location: fwp\ikeext_cert_criteria_name_type.htm
tech.root: fwp
ms.assetid: ec59d6b2-3bfc-4e5b-9222-609d3141db5c
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_CRITERIA_CN, IKEEXT_CERT_CRITERIA_DC, IKEEXT_CERT_CRITERIA_DNS, IKEEXT_CERT_CRITERIA_NAME_TYPE, IKEEXT_CERT_CRITERIA_NAME_TYPE enumeration [Filtering], IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX, IKEEXT_CERT_CRITERIA_O, IKEEXT_CERT_CRITERIA_OU, IKEEXT_CERT_CRITERIA_RFC822, IKEEXT_CERT_CRITERIA_UPN, fwp.ikeext_cert_criteria_name_type, iketypes/IKEEXT_CERT_CRITERIA_CN, iketypes/IKEEXT_CERT_CRITERIA_DC, iketypes/IKEEXT_CERT_CRITERIA_DNS, iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE, iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX, iketypes/IKEEXT_CERT_CRITERIA_O, iketypes/IKEEXT_CERT_CRITERIA_OU, iketypes/IKEEXT_CERT_CRITERIA_RFC822, iketypes/IKEEXT_CERT_CRITERIA_UPN
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
req.typenames: IKEEXT_CERT_CRITERIA_NAME_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERT_CRITERIA_NAME_TYPE_
 - iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE_
 - IKEEXT_CERT_CRITERIA_NAME_TYPE
 - iketypes/IKEEXT_CERT_CRITERIA_NAME_TYPE
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
 - IKEEXT_CERT_CRITERIA_NAME_TYPE
---

# IKEEXT_CERT_CRITERIA_NAME_TYPE enumeration


## -description

The <b>IKEEXT_CERT_CRITERIA_NAME_TYPE</b> enumerated type specifies the type of NAME fields possible for a certificate selection "subject" criteria.

## -enum-fields

### -field IKEEXT_CERT_CRITERIA_DNS:0

DNS name in the Subject Alternative Name of the certificate.

### -field IKEEXT_CERT_CRITERIA_UPN

UPN name in the Subject Alternative Name of the certificate.

### -field IKEEXT_CERT_CRITERIA_RFC822

RFC 822 name in the Subject Alternative Name of the certificate.

### -field IKEEXT_CERT_CRITERIA_CN

CN in the Subject of the certificate.

### -field IKEEXT_CERT_CRITERIA_OU

OU in the Subject of the certificate.

### -field IKEEXT_CERT_CRITERIA_O

O in the Subject of the certificate.

### -field IKEEXT_CERT_CRITERIA_DC

DC in the Subject of the certificate.

### -field IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX

Maximum value for testing purposes.

