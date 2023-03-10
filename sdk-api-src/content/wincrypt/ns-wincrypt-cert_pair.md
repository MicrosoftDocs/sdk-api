---
UID: NS:wincrypt._CERT_PAIR
title: CERT_PAIR (wincrypt.h)
description: The CERT_PAIR structure contains a certificate and its pair cross certificate.
helpviewer_keywords: ["*PCERT_PAIR","CERT_PAIR","CERT_PAIR structure [Security]","PCERT_PAIR","PCERT_PAIR structure pointer [Security]","_crypto2_cert_pair","security.cert_pair","wincrypt/CERT_PAIR","wincrypt/PCERT_PAIR"]
old-location: security\cert_pair.htm
tech.root: security
ms.assetid: b5929430-1b12-4ebf-a5ef-3669bba63f8c
ms.date: 12/05/2018
ms.keywords: '*PCERT_PAIR, CERT_PAIR, CERT_PAIR structure [Security], PCERT_PAIR, PCERT_PAIR structure pointer [Security], _crypto2_cert_pair, security.cert_pair, wincrypt/CERT_PAIR, wincrypt/PCERT_PAIR'
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
req.typenames: CERT_PAIR, *PCERT_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_PAIR
 - wincrypt/_CERT_PAIR
 - PCERT_PAIR
 - wincrypt/PCERT_PAIR
 - CERT_PAIR
 - wincrypt/CERT_PAIR
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
 - CERT_PAIR
---

# CERT_PAIR structure


## -description

The <b>CERT_PAIR</b> structure contains a certificate and its pair cross certificate.

## -struct-fields

### -field Forward

An optional <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> structure that contains a certificate. If the <b>cbData</b> member of <b>Forward</b> is zero, the certificate may be empty.

### -field Reverse

An optional <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> structure that contains a certificate. If the <b>cbData</b> member of <b>Reverse</b> is zero, the certificate may be empty.