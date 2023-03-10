---
UID: NS:wincrypt._CERT_TRUST_LIST_INFO
title: CERT_TRUST_LIST_INFO (wincrypt.h)
description: The CERT_TRUST_LIST_INFO structure that indicates valid usage of a CTL.
helpviewer_keywords: ["*PCERT_TRUST_LIST_INFO","CERT_TRUST_LIST_INFO","CERT_TRUST_LIST_INFO structure [Security]","PCERT_TRUST_LIST_INFO","PCERT_TRUST_LIST_INFO structure pointer [Security]","_crypto2_cert_trust_list_info","security.cert_trust_list_info","wincrypt/CERT_TRUST_LIST_INFO","wincrypt/PCERT_TRUST_LIST_INFO"]
old-location: security\cert_trust_list_info.htm
tech.root: security
ms.assetid: 774f5626-9b48-4585-b713-adbf191861cc
ms.date: 12/05/2018
ms.keywords: '*PCERT_TRUST_LIST_INFO, CERT_TRUST_LIST_INFO, CERT_TRUST_LIST_INFO structure [Security], PCERT_TRUST_LIST_INFO, PCERT_TRUST_LIST_INFO structure pointer [Security], _crypto2_cert_trust_list_info, security.cert_trust_list_info, wincrypt/CERT_TRUST_LIST_INFO, wincrypt/PCERT_TRUST_LIST_INFO'
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
req.typenames: CERT_TRUST_LIST_INFO, *PCERT_TRUST_LIST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_TRUST_LIST_INFO
 - wincrypt/_CERT_TRUST_LIST_INFO
 - PCERT_TRUST_LIST_INFO
 - wincrypt/PCERT_TRUST_LIST_INFO
 - CERT_TRUST_LIST_INFO
 - wincrypt/CERT_TRUST_LIST_INFO
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
 - CERT_TRUST_LIST_INFO
---

# CERT_TRUST_LIST_INFO structure


## -description

The <b>CERT_TRUST_LIST_INFO</b> structure that indicates valid usage of a CTL.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field pCtlEntry

A pointer to a structure that includes a subject identifier, the count of attributes associated with a CTL, and an array of those attributes.

### -field pCtlContext

A pointer to a CTL context.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_element">CERT_CHAIN_ELEMENT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a>