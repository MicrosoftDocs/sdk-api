---
UID: NC:cryptxml.CryptXmlDllGetInterface
title: CryptXmlDllGetInterface
author: windows-sdk-content
description: Retrieves a pointer to the cryptographic extension functions for the specified algorithm.
old-location: security\cryptxmldllgetinterface.htm
tech.root: seccrypto
ms.assetid: a547e869-3c9f-4408-9895-29fae0cc6066
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CryptXmlDllGetInterface, CryptXmlDllGetInterface callback, CryptXmlDllGetInterface callback function [Security], cryptxml/CryptXmlDllGetInterface, security.cryptxmldllgetinterface
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
 - CryptXmlDllGetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllGetInterface callback function


## -description


The <b>CryptXmlDllGetInterface</b> function retrieves a pointer to the cryptographic extension functions for the specified algorithm.


## -parameters




### -param dwFlags

This parameter is reserved and must be set to zero.


### -param *pMethod [in]

A pointer to a <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure to retrieve the interface of.


### -param *pInterface [out]

A pointer to a <a href="https://msdn.microsoft.com/ab6ec092-d25d-4ca0-8206-b7e5ad36d69b">CRYPT_XML_ALGORITHM_INFO</a> structure to receive the interface information.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




## -remarks



The cryptographic extensions DLL must export the <b>CryptXmlDllGetInterface</b> entry.


To get the <a href="https://msdn.microsoft.com/55585a57-be3e-492d-bf56-4e2456572161">CRYPT_XML_CRYPTOGRAPHIC_INTERFACE</a>  table, CryptXml loads the registered cryptographic extensions DLL by using the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function, and then it calls the
<b>CryptXmlDllGetInterface</b> function.




