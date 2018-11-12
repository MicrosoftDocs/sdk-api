---
UID: NC:cryptxml.CryptXmlDllFinalizeDigest
title: CryptXmlDllFinalizeDigest
author: windows-sdk-content
description: Retrieves the digest value.
old-location: security\cryptxmldllfinalizedigest.htm
tech.root: seccrypto
ms.assetid: 749226fa-6de8-4c1c-9ec0-9801a2029a6e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CryptXmlDllFinalizeDigest, CryptXmlDllFinalizeDigest callback, CryptXmlDllFinalizeDigest callback function [Security], cryptxml/CryptXmlDllFinalizeDigest, security.cryptxmldllfinalizedigest
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
 - CryptXmlDllFinalizeDigest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllFinalizeDigest callback function


## -description


The <b>CryptXmlDllFinalizeDigest</b> function retrieves the digest value.

The <b>CryptXmlDllFinalizeDigest</b> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param hDigest [in]

The handle of the hash object used to put data into the digest. This handle is obtained by calling the <a href="https://msdn.microsoft.com/9c9b14c8-511b-4e40-b3d3-014d75dc7fe4">CryptXmlDllCreateDigest</a>  function.


### -param *pbDigest [out]

A pointer to a buffer that receives the digest value.


### -param cbDigest

The size, in bytes, of the buffer pointed to by the <i>pbDigest</i> parameter.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



