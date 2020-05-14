---
UID: NC:cryptxml.CryptXmlDllCloseDigest
title: CryptXmlDllCloseDigest (cryptxml.h)
description: Frees the CRYPT_XML_DIGEST allocated by the CryptXmlDllCreateDigest function.helpviewer_keywords: ["CryptXmlDllCloseDigest","CryptXmlDllCloseDigest callback","CryptXmlDllCloseDigest callback function [Security]","cryptxml/CryptXmlDllCloseDigest","security.cryptxmldllclosedigest"]
old-location: security\cryptxmldllclosedigest.htm
tech.root: SecCrypto
ms.assetid: 97f720b9-f937-4469-abe9-62bf35ebdd7a
ms.date: 12/05/2018
ms.keywords: CryptXmlDllCloseDigest, CryptXmlDllCloseDigest callback, CryptXmlDllCloseDigest callback function [Security], cryptxml/CryptXmlDllCloseDigest, security.cryptxmldllclosedigest
f1_keywords:
- cryptxml/CryptXmlDllCloseDigest
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Cryptxml.h
api_name:
- CryptXmlDllCloseDigest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptXmlDllCloseDigest callback function


## -description


The <b>CryptXmlDllCloseDigest</b> function frees the CRYPT_XML_DIGEST allocated by the <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest">CryptXmlDllCreateDigest</a> function.

The <i>CryptXmlDllCloseDigest</i> function is exposed through the  Cryptographic Extensions DLL  and is exposed through the exported <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param hDigest [in]

The handle of the hash object. This handle is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest">CryptXmlCreateDigest</a>  function. After the function has been called, the digest handle passed to this function is released and cannot be used again.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



