---
UID: NS:wintrust.WINTRUST_CERT_INFO_
title: WINTRUST_CERT_INFO (wintrust.h)
description: Used when calling WinVerifyTrust to verify a CERT_CONTEXT.
helpviewer_keywords: ["*PWINTRUST_CERT_INFO","PWINTRUST_CERT_INFO","PWINTRUST_CERT_INFO structure pointer [Security]","WINTRUST_CERT_INFO","WINTRUST_CERT_INFO structure [Security]","_win32_wintrust_cert_info","security.wintrust_cert_info","wintrust/PWINTRUST_CERT_INFO","wintrust/WINTRUST_CERT_INFO"]
old-location: security\wintrust_cert_info.htm
tech.root: security
ms.assetid: 6522d1f0-3d96-4499-9220-23288122e0e6
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_CERT_INFO, PWINTRUST_CERT_INFO, PWINTRUST_CERT_INFO structure pointer [Security], WINTRUST_CERT_INFO, WINTRUST_CERT_INFO structure [Security], _win32_wintrust_cert_info, security.wintrust_cert_info, wintrust/PWINTRUST_CERT_INFO, wintrust/WINTRUST_CERT_INFO'
req.header: wintrust.h
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
req.typenames: WINTRUST_CERT_INFO, *PWINTRUST_CERT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_CERT_INFO_
 - wintrust/WINTRUST_CERT_INFO_
 - PWINTRUST_CERT_INFO
 - wintrust/PWINTRUST_CERT_INFO
 - WINTRUST_CERT_INFO
 - wintrust/WINTRUST_CERT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_CERT_INFO
---

# WINTRUST_CERT_INFO structure


## -description

<p class="CCE_Message">[The  <b>WINTRUST_CERT_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_CERT_INFO</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to verify a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

## -struct-fields

### -field cbStruct

Count of bytes in this structure.

### -field pcwszDisplayName

String with the name of the memory object pointed to by the <b>pbMem</b> member of the 
[WINTRUST_BLOB_INFO](/windows/desktop/api/wintrust/ns-wintrust-wintrust_blob_info) structure.

### -field psCertContext

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> to be verified.

### -field chStores

The number of store handles in <b>pahStores</b>.

### -field pahStores

An array of open <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a> to add to the list of stores that the policy provider looks in to find certificates while building a trust chain.

### -field dwFlags

### -field psftVerifyAsOf