---
UID: NF:wincrypt.CryptUnregisterDefaultOIDFunction
title: CryptUnregisterDefaultOIDFunction function
author: windows-sdk-content
description: The CryptUnregisterDefaultOIDFunction removes the registration of a DLL containing the default function to be called for the specified encoding type and function name.
old-location: security\cryptunregisterdefaultoidfunction.htm
tech.root: seccrypto
ms.assetid: 63f5b0c7-f574-4dc6-92c7-091f25febd48
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CryptUnregisterDefaultOIDFunction, CryptUnregisterDefaultOIDFunction function [Security], _crypto2_cryptunregisterdefaultoidfunction, security.cryptunregisterdefaultoidfunction, wincrypt/CryptUnregisterDefaultOIDFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptUnregisterDefaultOIDFunction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptUnregisterDefaultOIDFunction function


## -description


The <b>CryptUnregisterDefaultOIDFunction</b> removes the registration of a DLL containing the default function to be called for the specified encoding type and function name.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pszFuncName [in]

Name of the function being unregistered.


### -param pwszDll [in]

Name of the DLL where the function is located.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).




## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

