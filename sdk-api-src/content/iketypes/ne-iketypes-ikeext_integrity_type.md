---
UID: NE:iketypes.IKEEXT_INTEGRITY_TYPE_
title: IKEEXT_INTEGRITY_TYPE (iketypes.h)
description: Specifies the type of hash algorithm used for integrity protection of Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.
helpviewer_keywords: ["IKEEXT_INTEGRITY_MD5","IKEEXT_INTEGRITY_SHA1","IKEEXT_INTEGRITY_SHA_256","IKEEXT_INTEGRITY_SHA_384","IKEEXT_INTEGRITY_TYPE","IKEEXT_INTEGRITY_TYPE enumeration [Filtering]","IKEEXT_INTEGRITY_TYPE_MAX","fwp.ikeext_integrity_type","iketypes/IKEEXT_INTEGRITY_MD5","iketypes/IKEEXT_INTEGRITY_SHA1","iketypes/IKEEXT_INTEGRITY_SHA_256","iketypes/IKEEXT_INTEGRITY_SHA_384","iketypes/IKEEXT_INTEGRITY_TYPE","iketypes/IKEEXT_INTEGRITY_TYPE_MAX"]
old-location: fwp\ikeext_integrity_type.htm
tech.root: fwp
ms.assetid: f4a5b6b9-5cf1-48a4-811c-9150550688d8
ms.date: 12/05/2018
ms.keywords: IKEEXT_INTEGRITY_MD5, IKEEXT_INTEGRITY_SHA1, IKEEXT_INTEGRITY_SHA_256, IKEEXT_INTEGRITY_SHA_384, IKEEXT_INTEGRITY_TYPE, IKEEXT_INTEGRITY_TYPE enumeration [Filtering], IKEEXT_INTEGRITY_TYPE_MAX, fwp.ikeext_integrity_type, iketypes/IKEEXT_INTEGRITY_MD5, iketypes/IKEEXT_INTEGRITY_SHA1, iketypes/IKEEXT_INTEGRITY_SHA_256, iketypes/IKEEXT_INTEGRITY_SHA_384, iketypes/IKEEXT_INTEGRITY_TYPE, iketypes/IKEEXT_INTEGRITY_TYPE_MAX
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_INTEGRITY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_INTEGRITY_TYPE_
 - iketypes/IKEEXT_INTEGRITY_TYPE_
 - IKEEXT_INTEGRITY_TYPE
 - iketypes/IKEEXT_INTEGRITY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_INTEGRITY_TYPE
---

# IKEEXT_INTEGRITY_TYPE enumeration


## -description

The <b>IKEEXT_INTEGRITY_TYPE</b> enumerated type specifies the type of hash algorithm used for integrity protection of Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.

## -enum-fields

### -field IKEEXT_INTEGRITY_MD5:0

Specifies MD5 hash algorithm.

### -field IKEEXT_INTEGRITY_SHA1

Specifies SHA1 hash algorithm.

### -field IKEEXT_INTEGRITY_SHA_256

Specifies a 256-bit SHA encryption.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_INTEGRITY_SHA_384

Specifies a 384-bit SHA encryption.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_INTEGRITY_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
