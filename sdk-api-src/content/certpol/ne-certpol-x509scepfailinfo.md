---
UID: NE:certpol.X509SCEPFailInfo
title: X509SCEPFailInfo (certpol.h)
description: Describes the nature of an SCEP certificate enrollment failure.
helpviewer_keywords: ["SCEPFailBadAlgorithm","SCEPFailBadCertId","SCEPFailBadMessageCheck","SCEPFailBadRequest","SCEPFailBadTime","X509SCEPFailInfo","X509SCEPFailInfo enumeration [Security]","certpol/SCEPFailBadAlgorithm","certpol/SCEPFailBadCertId","certpol/SCEPFailBadMessageCheck","certpol/SCEPFailBadRequest","certpol/SCEPFailBadTime","certpol/X509SCEPFailInfo","security.x509scepfailinfo"]
old-location: security\x509scepfailinfo.htm
tech.root: security
ms.assetid: A2C314FB-A348-41CE-9736-2BDE05F7E70E
ms.date: 12/05/2018
ms.keywords: SCEPFailBadAlgorithm, SCEPFailBadCertId, SCEPFailBadMessageCheck, SCEPFailBadRequest, SCEPFailBadTime, X509SCEPFailInfo, X509SCEPFailInfo enumeration [Security], certpol/SCEPFailBadAlgorithm, certpol/SCEPFailBadCertId, certpol/SCEPFailBadMessageCheck, certpol/SCEPFailBadRequest, certpol/SCEPFailBadTime, certpol/X509SCEPFailInfo, security.x509scepfailinfo
req.header: certpol.h
req.include-header: CertEnroll.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: X509SCEPFailInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509SCEPFailInfo
 - certpol/X509SCEPFailInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - certpol.h
api_name:
 - X509SCEPFailInfo
---

# X509SCEPFailInfo enumeration


## -description

The <b>X509SCEPFailInfo</b> enumeration   describes the nature of an SCEP certificate enrollment failure. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a> interface.

## -enum-fields

### -field SCEPFailUnknown:-1

### -field SCEPFailBadAlgorithm:0

Failure due to an unrecognized or unsupported algorithm.

### -field SCEPFailBadMessageCheck:1

The integrity check failed.

### -field SCEPFailBadRequest:2

The transaction was not permitted or was not supported.

### -field SCEPFailBadTime:3

The signing time attribute from the PKCS7 authenticated attributes was not sufficiently close to the system time.

### -field SCEPFailBadCertId:4

No certificate could be identified.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_failinfo">FailInfo</a>
