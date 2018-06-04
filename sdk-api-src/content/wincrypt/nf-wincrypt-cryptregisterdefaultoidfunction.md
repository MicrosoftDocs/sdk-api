---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CryptRegisterDefaultOIDFunction function


## -description



			The <b>CryptRegisterDefaultOIDFunction</b> registers a DLL containing the default function to be called for the specified encoding type and function name. Unlike 
<a href="https://msdn.microsoft.com/b625597d-28fd-4a40-afbe-a09201d36512">CryptRegisterOIDFunction</a>, the function name to be exported by the DLL cannot be overridden.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pszFuncName [in]

Name of the function being registered.


### -param dwIndex [in]

Index location for the insertion of the DLL in the list of DLLs. If <i>dwIndex</i> is zero, the DLL is inserted at the beginning of the list. If it is CRYPT_REGISTER_LAST_INDEX, the DLL is appended at the end of the list.


### -param pwszDll [in]

Optional environment-variable string to be expanded using <a href="https://msdn.microsoft.com/b563e8ed-311d-4971-94f3-9c9fde4a2f30">ExpandEnvironmentStrings</a> function before loading the DLL.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).




## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

