---
UID: NC:cryptxml.CryptXmlDllGetInterface
title: CryptXmlDllGetInterface (cryptxml.h)
description: Retrieves a pointer to the cryptographic extension functions for the specified algorithm.
helpviewer_keywords: ["CryptXmlDllGetInterface","CryptXmlDllGetInterface callback","CryptXmlDllGetInterface callback function [Security]","cryptxml/CryptXmlDllGetInterface","security.cryptxmldllgetinterface"]
old-location: security\cryptxmldllgetinterface.htm
tech.root: security
ms.assetid: a547e869-3c9f-4408-9895-29fae0cc6066
ms.date: 12/05/2018
ms.keywords: CryptXmlDllGetInterface, CryptXmlDllGetInterface callback, CryptXmlDllGetInterface callback function [Security], cryptxml/CryptXmlDllGetInterface, security.cryptxmldllgetinterface
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
 - CryptXmlDllGetInterface
 - cryptxml/CryptXmlDllGetInterface
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
 - CryptXmlDllGetInterface
---

# CryptXmlDllGetInterface callback function


## -description

The <b>CryptXmlDllGetInterface</b> function retrieves a pointer to the cryptographic extension functions for the specified algorithm.

## -parameters

### -param dwFlags

This parameter is reserved and must be set to zero.

### -param pMethod [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure to retrieve the interface of.

### -param pInterface [out]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure to receive the interface information.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

The cryptographic extensions DLL must export the <b>CryptXmlDllGetInterface</b> entry.


To get the <a href="/windows/win32/api/cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface">CRYPT_XML_CRYPTOGRAPHIC_INTERFACE</a>  table, CryptXml loads the registered cryptographic extensions DLL by using the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function, and then it calls the
<b>CryptXmlDllGetInterface</b> function.
