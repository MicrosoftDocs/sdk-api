---
UID: NF:wincrypt.CryptGetOIDFunctionAddress
title: CryptGetOIDFunctionAddress function
author: windows-sdk-content
description: Searches the list of registered and installed functions for an encoding type and object identifier (OID) match.
old-location: security\cryptgetoidfunctionaddress.htm
tech.root: seccrypto
ms.assetid: 2eef6109-a840-48c6-936c-ec0875039c39
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CRYPT_GET_INSTALLED_OID_FUNC_FLAG, CryptGetOIDFunctionAddress, CryptGetOIDFunctionAddress function [Security], _crypto2_cryptgetoidfunctionaddress, security.cryptgetoidfunctionaddress, wincrypt/CryptGetOIDFunctionAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
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
 - CryptGetOIDFunctionAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptGetOIDFunctionAddress function


## -description


The <b>CryptGetOIDFunctionAddress</b> function searches the list of registered and installed functions for an encoding type and <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) match. If a match is found, the DLL that contains the function is, if necessary, loaded. If a match is found, a pointer to the function address and a pointer to the function handle are also returned. The <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the function handle is incremented.


## -parameters




### -param hFuncSet [in]

The function set handle previously obtained from a call to 
the <a href="https://msdn.microsoft.com/576a2989-ed7f-417d-b60e-24baf90a6554">CryptInitOIDFunctionSet</a> function.


### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are used; however, additional encoding types can be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

For functions that do not use an encoding type, set this parameter to zero.


### -param pszOID [in]

If the high-order word of the OID is nonzero, <i>pszOID</i> is a pointer to either an OID string such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string such as "file". If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier. This resulting OID maps to the function that was either installed or registered with the same OID.


### -param dwFlags [in]

This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_GET_INSTALLED_OID_FUNC_FLAG"></a><a id="crypt_get_installed_oid_func_flag"></a><dl>
<dt><b>CRYPT_GET_INSTALLED_OID_FUNC_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Searches only the installed list of functions.

</td>
</tr>
</table>
 


### -param ppvFuncAddr [out]

A pointer to a pointer to a function address. If a match is found, <i>ppvFuncAddr</i> points to the function address.


### -param phFuncAddr [out]

If a match is found, <i>phFuncAddr</i> points to the function handle. The <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> for the handle is incremented. 
When you have finished using the handle, release the handle by calling the <a href="https://msdn.microsoft.com/cacacff3-25b7-4ed4-885b-b4b0b326628f">CryptFreeOIDFunctionAddress</a> function. 




<div class="alert"><b>Note</b>  By default, both the registered and installed function lists are searched. To search only the installed list of functions, set CRYPT_GET_INSTALLED_OID_FUNC_FLAG. This flag would be set by a registered function to get the address of a preinstalled function it was replacing. For example, the registered function might handle a new special case and call the preinstalled function to handle the remaining cases.</div>
<div> </div>

## -returns



If the function succeeds and a match is found, the function returns nonzero (<b>TRUE</b>).

If the function fails or no match is found, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can call <b>CryptGetOIDFunctionAddress</b> with the <i>pszOID</i> argument set to <b>CMSG_DEFAULT_INSTALLABLE_FUNC_OID</b> to get the default installable function for the following callback functions.

For retrieval of the default functions, set <i>dwEncodingType</i> to a bitwise <b>OR</b> combination of the following encoding types.

<b>CRYPT_ASN_ENCODING</b>
<b>X509_ASN_ENCODING</b>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">OID Support Functions</a>
 

 

