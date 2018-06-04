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

# CryptInstallOIDFunctionAddress function


## -description


The <b>CryptInstallOIDFunctionAddress</b> function installs a set of callable <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) function addresses.


## -parameters




### -param hModule [in]

This parameter is updated with the <i>hModule</i> parameter passed to <b>DllMain</b> to prevent the DLL that contains the function addresses from being unloaded by 
<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a> or
<a href="https://msdn.microsoft.com/cacacff3-25b7-4ed4-885b-b4b0b326628f">CryptFreeOIDFunctionAddress</a>. This would be the case when the DLL has also registered OID functions through 
<a href="https://msdn.microsoft.com/b625597d-28fd-4a40-afbe-a09201d36512">CryptRegisterOIDFunction</a>.


### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING


### -param pszFuncName [in]

Name of the function set being installed.


### -param cFuncEntry [in]

Number of array elements in <i>rgFuncEntry</i>[].


### -param rgFuncEntry [in]

Array of <a href="https://msdn.microsoft.com/84c4aca8-ee38-455f-8330-58f512a6d12c">CRYPT_OID_FUNC_ENTRY</a> structures, each containing an OID and the starting address of its correlated routine. 
					

Default functions are installed by setting the <b>pszOID</b> member of the <a href="https://msdn.microsoft.com/84c4aca8-ee38-455f-8330-58f512a6d12c">CRYPT_OID_FUNC_ENTRY</a> structure for their array element to CRYPT_DEFAULT_OID.


### -param dwFlags [in]

By default, a new function set is installed at the end of the list of function sets. Setting the CRYPT_INSTALL_OID_FUNC_BEFORE_FLAG flag installs the function set at the beginning of the list.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/84c4aca8-ee38-455f-8330-58f512a6d12c">CRYPT_OID_FUNC_ENTRY</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

