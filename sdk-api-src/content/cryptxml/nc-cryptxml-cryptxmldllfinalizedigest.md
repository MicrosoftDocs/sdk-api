---
UID: NC:cryptxml.CryptXmlDllFinalizeDigest
title: CryptXmlDllFinalizeDigest (cryptxml.h)
description: Retrieves the digest value.
helpviewer_keywords: ["CryptXmlDllFinalizeDigest","CryptXmlDllFinalizeDigest callback","CryptXmlDllFinalizeDigest callback function [Security]","cryptxml/CryptXmlDllFinalizeDigest","security.cryptxmldllfinalizedigest"]
old-location: security\cryptxmldllfinalizedigest.htm
tech.root: security
ms.assetid: 749226fa-6de8-4c1c-9ec0-9801a2029a6e
ms.date: 12/05/2018
ms.keywords: CryptXmlDllFinalizeDigest, CryptXmlDllFinalizeDigest callback, CryptXmlDllFinalizeDigest callback function [Security], cryptxml/CryptXmlDllFinalizeDigest, security.cryptxmldllfinalizedigest
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - CryptXmlDllFinalizeDigest
 - cryptxml/CryptXmlDllFinalizeDigest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cryptxml.h
api_name:
 - CryptXmlDllFinalizeDigest
---

# CryptXmlDllFinalizeDigest callback function


## -description

The <b>CryptXmlDllFinalizeDigest</b> function retrieves the digest value.

The <b>CryptXmlDllFinalizeDigest</b> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param hDigest [in]

The handle of the hash object used to put data into the digest. This handle is obtained by calling the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest">CryptXmlDllCreateDigest</a>  function.

### -param pbDigest [out]

A pointer to a buffer that receives the digest value.

### -param cbDigest

The size, in bytes, of the buffer pointed to by the <i>pbDigest</i> parameter.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
