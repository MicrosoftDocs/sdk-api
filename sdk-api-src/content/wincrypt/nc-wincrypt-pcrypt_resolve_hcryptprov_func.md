---
UID: NC:wincrypt.PCRYPT_RESOLVE_HCRYPTPROV_FUNC
title: PCRYPT_RESOLVE_HCRYPTPROV_FUNC
author: windows-sdk-content
description: Returns a handle to a cryptographic service provider (CSP) by using the phCryptProv parameter to receive the key being imported.
old-location: security\pcrypt_resolve_hcryptprov_func.htm
tech.root: SecCrypto
ms.assetid: d3b2b942-bde5-4399-9412-95fe227cd546
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PCRYPT_RESOLVE_HCRYPTPROV_FUNC, PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback, PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback function [Security], security.pcrypt_resolve_hcryptprov_func, wincrypt/PCRYPT_RESOLVE_HCRYPTPROV_FUNC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - PCRYPT_RESOLVE_HCRYPTPROV_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback function


## -description


<p class="CCE_Message">[The <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> function returns a handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) by using the <i>phCryptProv</i> parameter to receive the key being imported.  It is a callback function called from the context of  the <a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a> function.  The function must be implemented by the developer to suit each application.


## -parameters




### -param *pPrivateKeyInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/63a5d1c2-88b3-45fa-94d3-2179cb8802c9">CRYPT_PRIVATE_KEY_INFO</a> structure that describes the key being imported.


### -param *phCryptProv [out]

A pointer to the  <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a>   to receive the CSP.


### -param pVoidResolveFunc [in]

The <b>pVoidResolveFunc</b> member passed in by the caller in the <a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a>  structure.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="https://msdn.microsoft.com/63a5d1c2-88b3-45fa-94d3-2179cb8802c9">CRYPT_PRIVATE_KEY_INFO</a>



<a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a>



<a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a>
 

 

