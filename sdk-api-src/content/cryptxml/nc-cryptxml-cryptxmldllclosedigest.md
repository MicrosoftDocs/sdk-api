---
UID: NC:cryptxml.CryptXmlDllCloseDigest
title: CryptXmlDllCloseDigest
author: windows-sdk-content
description: Frees the CRYPT_XML_DIGEST allocated by the CryptXmlDllCreateDigest function.
old-location: security\cryptxmldllclosedigest.htm
tech.root: seccrypto
ms.assetid: 97f720b9-f937-4469-abe9-62bf35ebdd7a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptXmlDllCloseDigest, CryptXmlDllCloseDigest callback, CryptXmlDllCloseDigest callback function [Security], cryptxml/CryptXmlDllCloseDigest, security.cryptxmldllclosedigest
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CryptXmlDllCloseDigest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllCloseDigest callback function


## -description


The <b>CryptXmlDllCloseDigest</b> function frees the CRYPT_XML_DIGEST allocated by the <a href="https://msdn.microsoft.com/9c9b14c8-511b-4e40-b3d3-014d75dc7fe4">CryptXmlDllCreateDigest</a> function.

The <i>CryptXmlDllCloseDigest</i> function is exposed through the  Cryptographic Extensions DLL  and is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param hDigest [in]

The handle of the hash object. This handle is obtained by calling the <a href="https://msdn.microsoft.com/9c9b14c8-511b-4e40-b3d3-014d75dc7fe4">CryptXmlCreateDigest</a>  function. After the function has been called, the digest handle passed to this function is released and cannot be used again.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



