---
UID: NS:wincrypt._CERT_EXTENSIONS
title: CERT_EXTENSIONS (wincrypt.h)
description: The CERT_EXTENSIONS structure contains an array of extensions.
helpviewer_keywords: ["*PCERT_EXTENSIONS","CERT_EXTENSIONS","CERT_EXTENSIONS structure [Security]","PCERT_EXTENSIONS","PCERT_EXTENSIONS structure pointer [Security]","_crypto2_cert_extensions","security.cert_extensions","wincrypt/CERT_EXTENSIONS","wincrypt/PCERT_EXTENSIONS"]
old-location: security\cert_extensions.htm
tech.root: security
ms.assetid: b393ef08-cedb-4840-a427-10ead315d6ea
ms.date: 12/05/2018
ms.keywords: '*PCERT_EXTENSIONS, CERT_EXTENSIONS, CERT_EXTENSIONS structure [Security], PCERT_EXTENSIONS, PCERT_EXTENSIONS structure pointer [Security], _crypto2_cert_extensions, security.cert_extensions, wincrypt/CERT_EXTENSIONS, wincrypt/PCERT_EXTENSIONS'
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
req.typenames: CERT_EXTENSIONS, *PCERT_EXTENSIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_EXTENSIONS
 - wincrypt/_CERT_EXTENSIONS
 - PCERT_EXTENSIONS
 - wincrypt/PCERT_EXTENSIONS
 - CERT_EXTENSIONS
 - wincrypt/CERT_EXTENSIONS
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
 - CERT_EXTENSIONS
---

# CERT_EXTENSIONS structure


## -description

The <b>CERT_EXTENSIONS</b> structure contains an array of extensions.

## -struct-fields

### -field cExtension

Number of elements in the array <b>rgExtension</b>.

### -field rgExtension

Array of structures, each holding information of type <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> about a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> or <a href="/windows/desktop/SecGloss/c-gly">CRL</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>