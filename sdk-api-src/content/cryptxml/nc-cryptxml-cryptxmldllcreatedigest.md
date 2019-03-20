---
UID: NC:cryptxml.CryptXmlDllCreateDigest
title: CryptXmlDllCreateDigest (cryptxml.h)
author: windows-sdk-content
description: Creates a digest object for the specified method.
old-location: security\cryptxmldllcreatedigest.htm
tech.root: SecCrypto
ms.assetid: 9c9b14c8-511b-4e40-b3d3-014d75dc7fe4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptXmlDllCreateDigest, CryptXmlDllCreateDigest callback, CryptXmlDllCreateDigest callback function [Security], cryptxml/CryptXmlDllCreateDigest, security.cryptxmldllcreatedigest
ms.topic: callback
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
 - CryptXmlDllCreateDigest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllCreateDigest callback function


## -description


The <b>CryptXmlDllCreateDigest</b> function creates a digest object for the specified method.

The <b>CryptXmlDllCreateDigest</b> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param *pDigestMethod [in]

A pointer to a <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm to use to create the  digest.


### -param *pcbSize [out]

A pointer to a <b>ULONG</b> variable that receives the size, in bytes, of the digest.


### -param *phDigest [out]

A pointer to a <b>CRYPT_XML_DIGEST</b> variable  that receives a pointer to the digest.

When you have finished using the resources allocated by the call to this function, you must free them by calling the <a href="https://msdn.microsoft.com/97f720b9-f937-4469-abe9-62bf35ebdd7a">CryptXmlDllCloseDigest</a> function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



