---
UID: NC:cryptxml.CryptXmlDllGetAlgorithmInfo
title: CryptXmlDllGetAlgorithmInfo (cryptxml.h)
author: windows-sdk-content
description: Decodes the XML algorithm and returns information about the algorithm.
old-location: security\cryptxmldllgetalgorithminfo.htm
tech.root: SecCrypto
ms.assetid: 36af2809-0dbb-4024-926c-7054b734e97c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptXmlDllGetAlgorithmInfo, CryptXmlDllGetAlgorithmInfo callback, CryptXmlDllGetAlgorithmInfo callback function [Security], cryptxml/CryptXmlDllGetAlgorithmInfo, security.cryptxmldllgetalgorithminfo
ms.topic: callback
f1_keywords: 
 - "cryptxml/CryptXmlDllGetAlgorithmInfo"
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
ms.custom: 19H1
---

# CryptXmlDllGetAlgorithmInfo callback function


## -description


The <b>CryptXmlDllGetAlgorithmInfo</b> function decodes the XML algorithm and returns information about the algorithm.

The <b>CryptXmlDllGetAlgorithmInfo</b> function is exposed through the exported <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface">CryptXmlDllGetInterface</a>  function.


## -parameters




### -param *pXmlAlgorithm [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ns-cryptxml-_crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the algorithm.


#### - **ppAlgInfo [out]

A pointer to a pointer to a  <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ns-cryptxml-_crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure.

When you have finished using the memory pointed to by the <i>ppAlgInfo</i> parameter, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.


#### - ppAlgInfo [out]

A pointer to a pointer to a  <a href="https://docs.microsoft.com/windows/desktop/api/cryptxml/ns-cryptxml-_crypt_xml_algorithm_info">CRYPT_XML_ALGORITHM_INFO</a> structure.

When you have finished using the memory pointed to by the <i>ppAlgInfo</i> parameter, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



