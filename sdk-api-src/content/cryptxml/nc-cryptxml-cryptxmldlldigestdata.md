---
UID: NC:cryptxml.CryptXmlDllDigestData
title: CryptXmlDllDigestData (cryptxml.h)
description: Puts data into the digest.
helpviewer_keywords: ["CryptXmlDllDigestData","CryptXmlDllDigestData callback","CryptXmlDllDigestData callback function [Security]","cryptxml/CryptXmlDllDigestData","security.cryptxmldlldigestdata"]
old-location: security\cryptxmldlldigestdata.htm
tech.root: security
ms.assetid: b18a6e96-f5ed-4e48-af8c-4599c1864bf4
ms.date: 12/05/2018
ms.keywords: CryptXmlDllDigestData, CryptXmlDllDigestData callback, CryptXmlDllDigestData callback function [Security], cryptxml/CryptXmlDllDigestData, security.cryptxmldlldigestdata
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
 - CryptXmlDllDigestData
 - cryptxml/CryptXmlDllDigestData
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
 - CryptXmlDllDigestData
---

## -description

The <b>CryptXmlDllDigestData</b> function puts data into the digest.

The <b>CryptXmlDllDigestData</b> function is exposed through the exported <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.

## -parameters

### -param hDigest

The handle of the hash object used to put data into the digest. This handle is obtained by calling the <a href="/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest">CryptXmlDllCreateDigest</a>  function.

### -param pbData

A pointer to a block of data to be processed.

### -param cbData

The size, in bytes, of the block of data pointed to by the <i>pbData</i> parameter.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.