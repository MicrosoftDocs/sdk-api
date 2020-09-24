---
UID: NF:wincrypt.CertAddRefServerOcspResponseContext
title: CertAddRefServerOcspResponseContext function (wincrypt.h)
description: Increments the reference count for a CERT_SERVER_OCSP_RESPONSE_CONTEXT structure.
helpviewer_keywords: ["CertAddRefServerOcspResponseContext","CertAddRefServerOcspResponseContext function [Security]","security.certaddrefserverocspresponsecontext","wincrypt/CertAddRefServerOcspResponseContext"]
old-location: security\certaddrefserverocspresponsecontext.htm
tech.root: security
ms.assetid: b7cdce9b-25fe-4fb9-b266-61989793699b
ms.date: 12/05/2018
ms.keywords: CertAddRefServerOcspResponseContext, CertAddRefServerOcspResponseContext function [Security], security.certaddrefserverocspresponsecontext, wincrypt/CertAddRefServerOcspResponseContext
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
 - CertAddRefServerOcspResponseContext
 - wincrypt/CertAddRefServerOcspResponseContext
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
 - CertAddRefServerOcspResponseContext
---

# CertAddRefServerOcspResponseContext function


## -description

The <b>CertAddRefServerOcspResponseContext</b> function increments the reference count for a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure.

## -parameters

### -param pServerOcspResponseContext [in]

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> returned by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetserverocspresponsecontext">CertGetServerOcspResponseContext</a>.

## -remarks

Each call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetserverocspresponsecontext">CertGetServerOcspResponseContext</a> and <b>CertAddRefServerOcspResponseContext</b> requires a corresponding call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreeserverocspresponsecontext">CertFreeServerOcspResponseContext</a>.