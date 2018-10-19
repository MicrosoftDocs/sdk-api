---
UID: NC:cryptxml.CryptXmlDllDigestData
title: CryptXmlDllDigestData
author: windows-sdk-content
description: Puts data into the digest.
old-location: security\cryptxmldlldigestdata.htm
tech.root: seccrypto
ms.assetid: b18a6e96-f5ed-4e48-af8c-4599c1864bf4
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CryptXmlDllDigestData, CryptXmlDllDigestData callback, CryptXmlDllDigestData callback function [Security], cryptxml/CryptXmlDllDigestData, security.cryptxmldlldigestdata
ms.prod: windows
ms.technology: windows-sdk
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
 - CryptXmlDllDigestData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllDigestData callback function


## -description


The <b>CryptXmlDllDigestData</b> function puts data into the digest.

The <b>CryptXmlDllDigestData</b> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param hDigest

The handle of the hash object used to put data into the digest. This handle is obtained by calling the <a href="https://msdn.microsoft.com/9c9b14c8-511b-4e40-b3d3-014d75dc7fe4">CryptXmlDllCreateDigest</a>  function.


### -param *pbData

A pointer to a block of data to be processed.


### -param cbData








#### - cbDigest

The size, in bytes, of the block of data pointed to by the <i>pbData</i> parameter.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



