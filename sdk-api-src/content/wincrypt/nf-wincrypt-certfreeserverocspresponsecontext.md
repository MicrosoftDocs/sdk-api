---
UID: NF:wincrypt.CertFreeServerOcspResponseContext
title: CertFreeServerOcspResponseContext function (wincrypt.h)
description: Decrements the reference count for a CERT_SERVER_OCSP_RESPONSE_CONTEXT structure.
helpviewer_keywords: ["CertFreeServerOcspResponseContext","CertFreeServerOcspResponseContext function [Security]","security.certfreeserverocspresponsecontext","wincrypt/CertFreeServerOcspResponseContext"]
old-location: security\certfreeserverocspresponsecontext.htm
tech.root: security
ms.assetid: a07fc1e0-6f06-4336-b33c-d4d6a838b609
ms.date: 12/05/2018
ms.keywords: CertFreeServerOcspResponseContext, CertFreeServerOcspResponseContext function [Security], security.certfreeserverocspresponsecontext, wincrypt/CertFreeServerOcspResponseContext
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
 - CertFreeServerOcspResponseContext
 - wincrypt/CertFreeServerOcspResponseContext
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
 - CertFreeServerOcspResponseContext
---

# CertFreeServerOcspResponseContext function


## -description

The <b>CertFreeServerOcspResponseContext</b> function decrements the reference count for a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure. If the reference count becomes zero, memory allocated for the structure is released.

## -parameters

### -param pServerOcspResponseContext [in]

A pointer to a <a href="/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure that contains a value returned by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetserverocspresponsecontext">CertGetServerOcspResponseContext</a> function.