---
UID: NF:wincrypt.PFXIsPFXBlob
title: PFXIsPFXBlob function (wincrypt.h)
description: The PFXIsPFXBlob function attempts to decode the outer layer of a BLOB as a PFX packet.
helpviewer_keywords: ["PFXIsPFXBlob","PFXIsPFXBlob function [Security]","_crypto2_pfxispfxblob","security.pfxispfxblob","wincrypt/PFXIsPFXBlob"]
old-location: security\pfxispfxblob.htm
tech.root: security
ms.assetid: 28984407-0a28-48e1-9d67-37a6e9db7601
ms.date: 12/05/2018
ms.keywords: PFXIsPFXBlob, PFXIsPFXBlob function [Security], _crypto2_pfxispfxblob, security.pfxispfxblob, wincrypt/PFXIsPFXBlob
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - PFXIsPFXBlob
 - wincrypt/PFXIsPFXBlob
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
 - PFXIsPFXBlob
---

# PFXIsPFXBlob function


## -description

The <b>PFXIsPFXBlob</b> function attempts to decode the outer layer of a BLOB as a PFX packet.

## -parameters

### -param pPFX [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that the function will attempt to decode as a PFX packet.

## -returns

The function returns <b>TRUE</b> if the BLOB can be decoded as a PFX packet. If the outer layer of the BLOB cannot be decoded as a PFX packet, the function returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxverifypassword">PFXVerifyPassword</a>