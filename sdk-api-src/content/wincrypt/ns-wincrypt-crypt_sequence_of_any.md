---
UID: NS:wincrypt._CRYPT_SEQUENCE_OF_ANY
title: CRYPT_SEQUENCE_OF_ANY (wincrypt.h)
description: Contains an arbitrary list of encoded BLOBs.
helpviewer_keywords: ["*PCRYPT_SEQUENCE_OF_ANY","CRYPT_SEQUENCE_OF_ANY","CRYPT_SEQUENCE_OF_ANY structure [Security]","PCRYPT_SEQUENCE_OF_ANY","PCRYPT_SEQUENCE_OF_ANY structure pointer [Security]","_crypto2_crypt_sequence_of_any","security.crypt_sequence_of_any","wincrypt/CRYPT_SEQUENCE_OF_ANY","wincrypt/PCRYPT_SEQUENCE_OF_ANY"]
old-location: security\crypt_sequence_of_any.htm
tech.root: security
ms.assetid: 9500fa37-742b-4d37-8f45-0fb3c4cdda8d
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_SEQUENCE_OF_ANY, CRYPT_SEQUENCE_OF_ANY, CRYPT_SEQUENCE_OF_ANY structure [Security], PCRYPT_SEQUENCE_OF_ANY, PCRYPT_SEQUENCE_OF_ANY structure pointer [Security], _crypto2_crypt_sequence_of_any, security.crypt_sequence_of_any, wincrypt/CRYPT_SEQUENCE_OF_ANY, wincrypt/PCRYPT_SEQUENCE_OF_ANY'
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
req.typenames: CRYPT_SEQUENCE_OF_ANY, *PCRYPT_SEQUENCE_OF_ANY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_SEQUENCE_OF_ANY
 - wincrypt/_CRYPT_SEQUENCE_OF_ANY
 - PCRYPT_SEQUENCE_OF_ANY
 - wincrypt/PCRYPT_SEQUENCE_OF_ANY
 - CRYPT_SEQUENCE_OF_ANY
 - wincrypt/CRYPT_SEQUENCE_OF_ANY
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
 - CRYPT_SEQUENCE_OF_ANY
---

# CRYPT_SEQUENCE_OF_ANY structure


## -description

The <b>CRYPT_SEQUENCE_OF_ANY</b> structure contains an arbitrary list of encoded BLOBs.

## -struct-fields

### -field cValue

Number of elements in the <b>rgValue</b> array.

### -field rgValue

An array of 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structures.