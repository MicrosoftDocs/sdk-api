---
UID: NS:wincrypt._CERT_CREATE_CONTEXT_PARA
title: CERT_CREATE_CONTEXT_PARA (wincrypt.h)
description: Defines additional values that can be used when calling the CertCreateContext function.
helpviewer_keywords: ["*PCERT_CREATE_CONTEXT_PARA","CERT_CREATE_CONTEXT_PARA","CERT_CREATE_CONTEXT_PARA structure [Security]","security.cert_create_context_para","wincrypt/CERT_CREATE_CONTEXT_PARA"]
old-location: security\cert_create_context_para.htm
tech.root: security
ms.assetid: 1486cb60-56f0-4ce4-b283-6f92dcbbea26
ms.date: 12/05/2018
ms.keywords: '*PCERT_CREATE_CONTEXT_PARA, CERT_CREATE_CONTEXT_PARA, CERT_CREATE_CONTEXT_PARA structure [Security], security.cert_create_context_para, wincrypt/CERT_CREATE_CONTEXT_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CERT_CREATE_CONTEXT_PARA, *PCERT_CREATE_CONTEXT_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CREATE_CONTEXT_PARA
 - wincrypt/_CERT_CREATE_CONTEXT_PARA
 - PCERT_CREATE_CONTEXT_PARA
 - wincrypt/PCERT_CREATE_CONTEXT_PARA
 - CERT_CREATE_CONTEXT_PARA
 - wincrypt/CERT_CREATE_CONTEXT_PARA
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
 - CERT_CREATE_CONTEXT_PARA
---

# CERT_CREATE_CONTEXT_PARA structure


## -description

The <b>CERT_CREATE_CONTEXT_PARA</b> structure defines additional values that can be used when calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pfnFree

A pointer to the function that  frees the <i>pbEncoded</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> function. The  <b>pfnFree</b> function is called when the context created by  <b>CertCreateContext</b> is freed. This value can be <b>NULL</b>, in which case the <i>pbEncoded</i> parameter of the <b>CertCreateContext</b> function is not freed.

### -field pvFree

The address of the memory that gets freed by the <b>pfnFree</b> function. If <b>pvFree</b> is <b>NULL</b>, then the <i>pbEncoded</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> function is freed.

### -field pfnSort

A <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a> function pointer that will be called for each sorted context entry.

This member is only present for a <b>CERT_STORE_CTL_CONTEXT</b> when the <b>CERT_CREATE_CONTEXT_SORTED_FLAG</b> flag is set in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> function. You must verify that this member is present before trying to access it by examining the <b>cbSize</b> member of this structure.

### -field pvSort

An application-defined value that will be passed in the <i>pvSort</i> parameter of the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a> callback function.

This member is only present for a <b>CERT_STORE_CTL_CONTEXT</b> when the <b>CERT_CREATE_CONTEXT_SORTED_FLAG</b> flag is set in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a> function. You must verify that this member is present before trying to access it by examining the <b>cbSize</b> member of this structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecontext">CertCreateContext</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a>