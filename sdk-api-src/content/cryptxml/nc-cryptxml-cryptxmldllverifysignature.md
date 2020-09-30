---
UID: NC:cryptxml.CryptXmlDllVerifySignature
title: CryptXmlDllVerifySignature (cryptxml.h)
description: Verifies a signature.
helpviewer_keywords: ["CryptXmlDllVerifySignature","CryptXmlDllVerifySignature callback","CryptXmlDllVerifySignature callback function [Security]","cryptxml/CryptXmlDllVerifySignature","security.cryptxmldllverifysignature"]
old-location: security\cryptxmldllverifysignature.htm
tech.root: security
ms.assetid: 6e864156-37bd-4f2a-b2e9-f7269aa70241
ms.date: 12/05/2018
ms.keywords: CryptXmlDllVerifySignature, CryptXmlDllVerifySignature callback, CryptXmlDllVerifySignature callback function [Security], cryptxml/CryptXmlDllVerifySignature, security.cryptxmldllverifysignature
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
 - CryptXmlDllVerifySignature
 - cryptxml/CryptXmlDllVerifySignature
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
 - CryptXmlDllVerifySignature
---

## -description

The <b>CryptXmlDllVerifySignature</b>  function verifies a signature.

The <b>CryptXmlDllVerifySignature</b> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param pSignatureMethod [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm.

### -param hKey [in]

A handle to the public key.

### -param pbInput [in]

A pointer to a buffer that contains the signed data. The <i>cbInput</i> parameter contains the size of this buffer.

### -param cbInput [in]

The size, in bytes, of the buffer pointed to by the <i>pbInput</i> parameter.

### -param pbSignature [in]

A pointer to a buffer that contains the signature value to be verified. The <i>cbSignature</i> parameter contains the size of this buffer.

### -param cbSignature [in]

The size, in bytes, of the <i>pbSignature</i> buffer.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.