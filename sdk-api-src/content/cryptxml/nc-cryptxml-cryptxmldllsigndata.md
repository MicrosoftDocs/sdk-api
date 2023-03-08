---
UID: NC:cryptxml.CryptXmlDllSignData
title: CryptXmlDllSignData (cryptxml.h)
description: Signs data. (CryptXmlDllSignData)
helpviewer_keywords: ["CryptXmlDllSignData","CryptXmlDllSignData callback","CryptXmlDllSignData callback function [Security]","cryptxml/CryptXmlDllSignData","security.cryptxmldllsigndata"]
old-location: security\cryptxmldllsigndata.htm
tech.root: security
ms.assetid: 6a159fd7-6bf2-43b7-ae7f-b4e4eb02615f
ms.date: 12/05/2018
ms.keywords: CryptXmlDllSignData, CryptXmlDllSignData callback, CryptXmlDllSignData callback function [Security], cryptxml/CryptXmlDllSignData, security.cryptxmldllsigndata
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
 - CryptXmlDllSignData
 - cryptxml/CryptXmlDllSignData
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
 - CryptXmlDllSignData
---

# CryptXmlDllSignData callback function


## -description

The <i>CryptXmlDllSignData</i> function signs data.

The <i>CryptXmlDllSignData</i> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param pSignatureMethod [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm.

### -param hCryptProvOrNCryptKey [in]

The handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) that creates the signature. This handle must be an <b>HCRYPTPROV</b> handle that was obtained from a call to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that was created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should pass in an <a href="/windows/desktop/SecCrypto/hcryptprov-or-ncrypt-key-handle">NCRYPT_KEY_HANDLE</a> handle.

### -param dwKeySpec [in]

The private key to use from the provider's container. This key can be AT_KEYEXCHANGE or AT_SIGNATURE. This parameter is ignored if an <b>NCRYPT_KEY_HANDLE</b> handle is used in the <i>hCryptProvOrNCryptKey</i> parameter.

### -param pbInput [in]

A pointer to a buffer that contains the digest value to sign. The <i>cbInput</i> parameter contains the size of this buffer.

### -param cbInput [in]

The size, in bytes, of the buffer pointed to by the <i>pbInput</i> parameter.

### -param pbOutput [out, optional]

The address of a buffer to receive the signature produced by this function. The <i>cbOutput</i> parameter contains the size of this buffer.

If this parameter is <b>NULL</b>, this function will calculate the size needed for the encrypted data and return the size in the location pointed to by the <i>pcbResult</i> parameter.

### -param cbOutput [in]

The size, in bytes, of the buffer pointed to by the <i>pbOutput</i> parameter.

### -param pcbResult [out]

A pointer to a <b>DWORD</b> variable that receives the number of bytes copied to the <i>pbOutput</i> buffer. 
If <i>pbOutput</i> is <b>NULL</b>, this receives the size, in bytes, required for the signature.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
