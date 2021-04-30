---
UID: NC:wincrypt.PFN_CERT_CREATE_CONTEXT_SORT_FUNC
title: PFN_CERT_CREATE_CONTEXT_SORT_FUNC (wincrypt.h)
description: Called for each sorted context entry when a context is created.
helpviewer_keywords: ["PFN_CERT_CREATE_CONTEXT_SORT_FUNC","PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback","PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback function [Security]","security.pfn_cert_create_context_sort_func","wincrypt/PFN_CERT_CREATE_CONTEXT_SORT_FUNC"]
old-location: security\pfn_cert_create_context_sort_func.htm
tech.root: security
ms.assetid: 5ad79970-d076-4e97-bf56-d6aad4b46eaa
ms.date: 12/05/2018
ms.keywords: PFN_CERT_CREATE_CONTEXT_SORT_FUNC, PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback, PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback function [Security], security.pfn_cert_create_context_sort_func, wincrypt/PFN_CERT_CREATE_CONTEXT_SORT_FUNC
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CERT_CREATE_CONTEXT_SORT_FUNC
 - wincrypt/PFN_CERT_CREATE_CONTEXT_SORT_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_CREATE_CONTEXT_SORT_FUNC
---

# PFN_CERT_CREATE_CONTEXT_SORT_FUNC callback function


## -description

The <b>PFN_CERT_CREATE_CONTEXT_SORT_FUNC</b> callback function is called for each sorted context entry when a context is created. This function pointer is passed in the <b>pfnSort</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_create_context_para">CERT_CREATE_CONTEXT_PARA</a> structure.

## -parameters

### -param cbTotalEncoded [in]

The total number of bytes of the encoded entries.

### -param cbRemainEncoded [in]

The number of bytes remaining to be encoded.

### -param cEntry [in]

The current number of sorted entries.

### -param pvSort [in, out]

An application-defined value that is passed in the <b>pvSort</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_create_context_para">CERT_CREATE_CONTEXT_PARA</a> structure.

## -returns

Return <b>TRUE</b> to continue the sort or <b>FALSE</b> to stop the sort. If <b>FALSE</b> is returned, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> will fail and set the last error code to <b>ERROR_CANCELLED</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_create_context_para">CERT_CREATE_CONTEXT_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a>
