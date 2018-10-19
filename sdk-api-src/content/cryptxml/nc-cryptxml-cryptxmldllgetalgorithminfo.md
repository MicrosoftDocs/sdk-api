---
UID: NC:cryptxml.CryptXmlDllGetAlgorithmInfo
title: CryptXmlDllGetAlgorithmInfo
author: windows-sdk-content
description: Decodes the XML algorithm and returns information about the algorithm.
old-location: security\cryptxmldllgetalgorithminfo.htm
tech.root: seccrypto
ms.assetid: 36af2809-0dbb-4024-926c-7054b734e97c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CryptXmlDllGetAlgorithmInfo, CryptXmlDllGetAlgorithmInfo callback, CryptXmlDllGetAlgorithmInfo callback function [Security], cryptxml/CryptXmlDllGetAlgorithmInfo, security.cryptxmldllgetalgorithminfo
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
 - CryptXmlDllGetAlgorithmInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllGetAlgorithmInfo callback function


## -description


The <b>CryptXmlDllGetAlgorithmInfo</b> function decodes the XML algorithm and returns information about the algorithm.

The <b>CryptXmlDllGetAlgorithmInfo</b> function is exposed through the exported <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param *pXmlAlgorithm [in]

A pointer to a <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm.


#### - **ppAlgInfo [out]

A pointer to a pointer to a  <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure.

When you have finished using the memory pointed to by the <i>ppAlgInfo</i> parameter, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


#### - ppAlgInfo [out]

A pointer to a pointer to a  <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure.

When you have finished using the memory pointed to by the <i>ppAlgInfo</i> parameter, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



