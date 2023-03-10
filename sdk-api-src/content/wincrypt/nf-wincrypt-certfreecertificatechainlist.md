---
UID: NF:wincrypt.CertFreeCertificateChainList
title: CertFreeCertificateChainList function (wincrypt.h)
description: Frees the array of pointers to chain contexts.
helpviewer_keywords: ["CertFreeCertificateChainList","CertFreeCertificateChainList function [Security]","security.certfreecertificatechainlist","wincrypt/CertFreeCertificateChainList"]
old-location: security\certfreecertificatechainlist.htm
tech.root: security
ms.assetid: a53b02ca-bc3f-43fd-8c90-2f646d550182
ms.date: 12/05/2018
ms.keywords: CertFreeCertificateChainList, CertFreeCertificateChainList function [Security], security.certfreecertificatechainlist, wincrypt/CertFreeCertificateChainList
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - CertFreeCertificateChainList
 - wincrypt/CertFreeCertificateChainList
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
 - CertFreeCertificateChainList
---

# CertFreeCertificateChainList function


## -description

The <b>CertFreeCertificateChainList</b> function frees the array of pointers to chain contexts.

## -parameters

### -param prgpSelection [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">PCCERT_CHAIN_CONTEXT</a> structure returned by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certselectcertificatechains">CertSelectCertificateChains</a> function.

## -remarks

 Before calling the <b>CertFreeCertificateChainList</b> function, you must call the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain">CertFreeCertificateChain</a> function on each chain context within the array pointed to by the <i>prgpSelection</i> parameter.