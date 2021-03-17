---
UID: NS:ntsecapi._KERB_CERTIFICATE_HASHINFO
title: KERB_CERTIFICATE_HASHINFO (ntsecapi.h)
description: Provides the payload information of the certificate hash.
helpviewer_keywords: ["*PKERB_CERTIFICATE_HASHINFO","KERB_CERTIFICATE_HASHINFO","KERB_CERTIFICATE_HASHINFO structure [Security]","PKERB_CERTIFICATE_HASHINFO","PKERB_CERTIFICATE_HASHINFO structure pointer [Security]","ntsecapi/KERB_CERTIFICATE_HASHINFO","ntsecapi/PKERB_CERTIFICATE_HASHINFO","security.kerb_certificate_hashinfo"]
old-location: security\kerb_certificate_hashinfo.htm
tech.root: security
ms.assetid: 09D78E91-5873-481D-A5FC-B7F39F8F9BB8
ms.date: 12/05/2018
ms.keywords: '*PKERB_CERTIFICATE_HASHINFO, KERB_CERTIFICATE_HASHINFO, KERB_CERTIFICATE_HASHINFO structure [Security], PKERB_CERTIFICATE_HASHINFO, PKERB_CERTIFICATE_HASHINFO structure pointer [Security], ntsecapi/KERB_CERTIFICATE_HASHINFO, ntsecapi/PKERB_CERTIFICATE_HASHINFO, security.kerb_certificate_hashinfo'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: KERB_CERTIFICATE_HASHINFO, *PKERB_CERTIFICATE_HASHINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_CERTIFICATE_HASHINFO
 - ntsecapi/_KERB_CERTIFICATE_HASHINFO
 - PKERB_CERTIFICATE_HASHINFO
 - ntsecapi/PKERB_CERTIFICATE_HASHINFO
 - KERB_CERTIFICATE_HASHINFO
 - ntsecapi/KERB_CERTIFICATE_HASHINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_CERTIFICATE_HASHINFO
---

# KERB_CERTIFICATE_HASHINFO structure


## -description

The <b>KERB_CERTIFICATE_HASHINFO</b> structure provides the payload information of the certificate hash.

## -struct-fields

### -field StoreNameLength

Length, in bytes, of the WCHAR string specifying the certificate store name. If <b>StoreNameLength</b> is zero, the "MY" certificate store is implied; otherwise the WCHAR string must immediately follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure in contiguous memory and must include a terminating null character.

### -field HashLength

Length, in bytes, of the certificate hash. The certificate hash data must follow the <b>KERB_CERTIFICATE_HASHINFO</b> structure and certificate store name (if present) in contiguous memory.

