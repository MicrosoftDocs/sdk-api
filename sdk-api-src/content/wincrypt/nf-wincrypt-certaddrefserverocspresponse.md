---
UID: NF:wincrypt.CertAddRefServerOcspResponse
title: CertAddRefServerOcspResponse function (wincrypt.h)
description: Increments the reference count for an HCERT_SERVER_OCSP_RESPONSE handle.
helpviewer_keywords: ["CertAddRefServerOcspResponse","CertAddRefServerOcspResponse function [Security]","security.certaddrefserverocspresponse","wincrypt/CertAddRefServerOcspResponse"]
old-location: security\certaddrefserverocspresponse.htm
tech.root: security
ms.assetid: 6ccc0e85-1fa0-480c-a5b4-b21ba811e5d0
ms.date: 12/05/2018
ms.keywords: CertAddRefServerOcspResponse, CertAddRefServerOcspResponse function [Security], security.certaddrefserverocspresponse, wincrypt/CertAddRefServerOcspResponse
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertAddRefServerOcspResponse
 - wincrypt/CertAddRefServerOcspResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertAddRefServerOcspResponse
---

# CertAddRefServerOcspResponse function


## -description

The <b>CertAddRefServerOcspResponse</b> function increments the reference count for an <b>HCERT_SERVER_OCSP_RESPONSE</b> handle.

## -parameters

### -param hServerOcspResponse [in]

A handle to an <b>HCERT_SERVER_OCSP_RESPONSE</b> returned by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a>.

## -remarks

Each <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a> and <b>CertAddRefServerOcspResponse</b> requires a corresponding <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcloseserverocspresponse">CertCloseServerOcspResponse</a>.