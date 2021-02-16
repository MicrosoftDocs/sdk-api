---
UID: NS:wincrypt._CERT_SERVER_OCSP_RESPONSE_CONTEXT
title: CERT_SERVER_OCSP_RESPONSE_CONTEXT (wincrypt.h)
description: Contains an encoded OCSP response.
helpviewer_keywords: ["*PCERT_SERVER_OCSP_RESPONSE_CONTEXT","CERT_SERVER_OCSP_RESPONSE_CONTEXT","CERT_SERVER_OCSP_RESPONSE_CONTEXT structure [Security]","PCCERT_SERVER_OCSP_RESPONSE_CONTEXT","PCCERT_SERVER_OCSP_RESPONSE_CONTEXT structure pointer [Security]","PCERT_SERVER_OCSP_RESPONSE_CONTEXT","PCERT_SERVER_OCSP_RESPONSE_CONTEXT structure pointer [Security]","security.cert_server_ocsp_response_context","wincrypt/CERT_SERVER_OCSP_RESPONSE_CONTEXT","wincrypt/PCCERT_SERVER_OCSP_RESPONSE_CONTEXT","wincrypt/PCERT_SERVER_OCSP_RESPONSE_CONTEXT"]
old-location: security\cert_server_ocsp_response_context.htm
tech.root: security
ms.assetid: 732e91a3-dcd2-491a-ba4f-e22b75b5a71e
ms.date: 12/05/2018
ms.keywords: '*PCERT_SERVER_OCSP_RESPONSE_CONTEXT, CERT_SERVER_OCSP_RESPONSE_CONTEXT, CERT_SERVER_OCSP_RESPONSE_CONTEXT structure [Security], PCCERT_SERVER_OCSP_RESPONSE_CONTEXT, PCCERT_SERVER_OCSP_RESPONSE_CONTEXT structure pointer [Security], PCERT_SERVER_OCSP_RESPONSE_CONTEXT, PCERT_SERVER_OCSP_RESPONSE_CONTEXT structure pointer [Security], security.cert_server_ocsp_response_context, wincrypt/CERT_SERVER_OCSP_RESPONSE_CONTEXT, wincrypt/PCCERT_SERVER_OCSP_RESPONSE_CONTEXT, wincrypt/PCERT_SERVER_OCSP_RESPONSE_CONTEXT'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_SERVER_OCSP_RESPONSE_CONTEXT, *PCERT_SERVER_OCSP_RESPONSE_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_SERVER_OCSP_RESPONSE_CONTEXT
 - wincrypt/_CERT_SERVER_OCSP_RESPONSE_CONTEXT
 - PCERT_SERVER_OCSP_RESPONSE_CONTEXT
 - wincrypt/PCERT_SERVER_OCSP_RESPONSE_CONTEXT
 - CERT_SERVER_OCSP_RESPONSE_CONTEXT
 - wincrypt/CERT_SERVER_OCSP_RESPONSE_CONTEXT
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
 - CERT_SERVER_OCSP_RESPONSE_CONTEXT
---

# CERT_SERVER_OCSP_RESPONSE_CONTEXT structure


## -description

The <b>CERT_SERVER_OCSP_RESPONSE_CONTEXT</b> structure contains an encoded OCSP response.

## -struct-fields

### -field cbSize

The size in bytes of this structure.

### -field pbEncodedOcspResponse

A pointer to the data buffer that contains the encoded OCSP response.

### -field cbEncodedOcspResponse

The size in bytes of <b>pbEncodedOcspResponse</b>.

