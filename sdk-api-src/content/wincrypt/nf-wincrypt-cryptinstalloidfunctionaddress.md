---
UID: NF:wincrypt.CryptInstallOIDFunctionAddress
title: CryptInstallOIDFunctionAddress function
author: windows-sdk-content
description: The CryptInstallOIDFunctionAddress function installs a set of callable object identifier (OID) function addresses.
old-location: security\cryptinstalloidfunctionaddress.htm
old-project: SecCrypto
ms.assetid: 934e8278-0e0b-4402-a2b6-ff1e913d54c9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CryptInstallOIDFunctionAddress, CryptInstallOIDFunctionAddress function [Security], _crypto2_cryptinstalloidfunctionaddress, security.cryptinstalloidfunctionaddress, wincrypt/CryptInstallOIDFunctionAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptInstallOIDFunctionAddress
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

