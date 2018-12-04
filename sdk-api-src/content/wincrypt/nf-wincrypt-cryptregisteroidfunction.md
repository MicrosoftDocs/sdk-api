---
UID: NF:wincrypt.CryptRegisterOIDFunction
title: CryptRegisterOIDFunction function
author: windows-sdk-content
description: Registers a DLL that contains the function to be called for the specified encoding type, function name, and object identifier (OID).
old-location: security\cryptregisteroidfunction.htm
tech.root: seccrypto
ms.assetid: b625597d-28fd-4a40-afbe-a09201d36512
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CryptRegisterOIDFunction, CryptRegisterOIDFunction function [Security], _crypto2_cryptregisteroidfunction, security.cryptregisteroidfunction, wincrypt/CryptRegisterOIDFunction
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
 - CryptRegisterOIDFunction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptRegisterOIDFunction function


## -description


The <b>CryptRegisterOIDFunction</b> function registers a DLL that contains the function to be called for the specified encoding type, function name, and <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

By default, new function names are installed at the end of the list. To register a new function before the installed functions, call 
the <a href="https://msdn.microsoft.com/3e167c5d-0000-4359-a7b0-9b3e4e64c50c">CryptSetOIDFunctionValue</a> function with <i>dwValueType</i> set to <b>REG_DWORD</b> and <i>pwszValueName</i> set to CRYPT_OID_REG_FLAGS_VALUE_NAME.

CRYPT_OID_REG_FLAGS_VALUE_NAME is defined as L"CryptFlags".

In addition to registering a DLL, the name of the function to be called can be overridden. For example, the <i>pszFuncName</i> parameter can be set to CryptDllEncodeObject and the <i>pszOverrideFuncName</i> parameter to MyEncodeXyz. The new form of CryptDllEncodeObject can then be referred to by using the name MyEncodeXyz. This allows a DLL to export multiple OID functions for the same function name without needing to interpose its own OID dispatcher function.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pszFuncName [in]

Name of the function being registered.


### -param pszOID [in]

OID of the function to be registered. If the high-order word of the OID is nonzero, <i>pszOID</i> is a pointer to either an OID string such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string such as "file." If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier.


### -param pwszDll [in]

Name of the DLL file to be registered. It can contain environment-variable strings to be expanded by using the <a href="https://msdn.microsoft.com/b563e8ed-311d-4971-94f3-9c9fde4a2f30">ExpandEnvironmentStrings</a> function before loading the DLL.


### -param pszOverrideFuncName [in]

String that specifies a name for the function exported in the DLL. If <i>pszOverrideFuncName</i> is <b>NULL</b>, the function name specified by <i>pszFuncName</i> is used.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).




## -remarks



When you have finished using an OID function, unregister it by calling the <a href="https://msdn.microsoft.com/c06ffda5-df7c-4e0e-bf4f-8b8c968fcd4c">CryptUnregisterOIDFunction</a>  function.




## -see-also




<a href="https://msdn.microsoft.com/3e167c5d-0000-4359-a7b0-9b3e4e64c50c">CryptSetOIDFunctionValue</a>



<a href="https://msdn.microsoft.com/c06ffda5-df7c-4e0e-bf4f-8b8c968fcd4c">CryptUnregisterOIDFunction</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

