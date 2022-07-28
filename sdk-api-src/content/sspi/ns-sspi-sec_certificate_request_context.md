---
UID: NS:sspi._SEC_CERTIFICATE_REQUEST_CONTEXT
tech.root: security
title: SEC_CERTIFICATE_REQUEST_CONTEXT
ms.date: 07/20/2022
targetos: Windows
description: Stores the certificate request context.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_CERTIFICATE_REQUEST_CONTEXT, *PSEC_CERTIFICATE_REQUEST_CONTEXT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_CERTIFICATE_REQUEST_CONTEXT
 - PSEC_CERTIFICATE_REQUEST_CONTEXT
 - SEC_CERTIFICATE_REQUEST_CONTEXT
f1_keywords:
 - _SEC_CERTIFICATE_REQUEST_CONTEXT
 - sspi/_SEC_CERTIFICATE_REQUEST_CONTEXT
 - PSEC_CERTIFICATE_REQUEST_CONTEXT
 - sspi/PSEC_CERTIFICATE_REQUEST_CONTEXT
 - SEC_CERTIFICATE_REQUEST_CONTEXT
 - sspi/SEC_CERTIFICATE_REQUEST_CONTEXT
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_CERTIFICATE_REQUEST_CONTEXT
---

## -description

Contains a TLS 1.3 certificate request context.

## -struct-fields

### -field cbCertificateRequestContext

The size (in bytes) of the **rgCertificateRequestContext** array.

### -field rgCertificateRequestContext

The TLS 1.3 certificate request context.

## -remarks

## -see-also
