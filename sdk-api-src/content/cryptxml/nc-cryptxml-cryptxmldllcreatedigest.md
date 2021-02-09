---
UID: NC:cryptxml.CryptXmlDllCreateDigest
title: CryptXmlDllCreateDigest (cryptxml.h)
description: Creates a digest object for the specified method.
helpviewer_keywords: ["CryptXmlDllCreateDigest","CryptXmlDllCreateDigest callback","CryptXmlDllCreateDigest callback function [Security]","cryptxml/CryptXmlDllCreateDigest","security.cryptxmldllcreatedigest"]
old-location: security\cryptxmldllcreatedigest.htm
tech.root: security
ms.assetid: 9c9b14c8-511b-4e40-b3d3-014d75dc7fe4
ms.date: 12/05/2018
ms.keywords: CryptXmlDllCreateDigest, CryptXmlDllCreateDigest callback, CryptXmlDllCreateDigest callback function [Security], cryptxml/CryptXmlDllCreateDigest, security.cryptxmldllcreatedigest
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
 - CryptXmlDllCreateDigest
 - cryptxml/CryptXmlDllCreateDigest
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
 - CryptXmlDllCreateDigest
---

# CryptXmlDllCreateDigest callback function


## -description

The <b>CryptXmlDllCreateDigest</b> function creates a digest object for the specified method.

The <b>CryptXmlDllCreateDigest</b> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param pDigestMethod [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm to use to create the  digest.

### -param pcbSize [out]

A pointer to a <b>ULONG</b> variable that receives the size, in bytes, of the digest.

### -param phDigest [out]

A pointer to a <b>CRYPT_XML_DIGEST</b> variable  that receives a pointer to the digest.

When you have finished using the resources allocated by the call to this function, you must free them by calling the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest">CryptXmlDllCloseDigest</a> function.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
