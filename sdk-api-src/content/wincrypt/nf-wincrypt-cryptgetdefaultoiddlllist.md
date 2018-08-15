---
UID: NF:wincrypt.CryptGetDefaultOIDDllList
title: CryptGetDefaultOIDDllList function
author: windows-sdk-content
description: The CryptGetDefaultOIDDllList function acquires the list of the names of DLL files that contain registered default object identifier (OID) functions for a specified function set and encoding type.
old-location: security\cryptgetdefaultoiddlllist.htm
old-project: seccrypto
ms.assetid: 9d4643c8-a582-4c19-bd77-33b94e953818
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptGetDefaultOIDDllList, CryptGetDefaultOIDDllList function [Security], _crypto2_cryptgetdefaultoiddlllist, security.cryptgetdefaultoiddlllist, wincrypt/CryptGetDefaultOIDDllList
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
 - CryptGetDefaultOIDDllList
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptGetDefaultOIDDllList function


## -description


The <b>CryptGetDefaultOIDDllList</b> function acquires the list of the names of DLL files that contain registered default <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) functions for a specified function set and encoding type.


## -parameters




### -param hFuncSet [in]

Function set handle previously obtained by a call to 
<a href="https://msdn.microsoft.com/576a2989-ed7f-417d-b60e-24baf90a6554">CryptInitOIDFunctionSet</a>.


### -param dwEncodingType [in]

Specifies the encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

<div class="alert"><b>Note</b>  Either a certificate or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> is required. X509_ASN_ENCODING is the default. If that type is indicated, it is used; otherwise, if the PKCS7_ASN_ENCODING type is indicated, it is used.</div>
<div> </div>

### -param pwszDllList [out]

A pointer to a buffer to receive the list of zero or more null-terminated file names. The returned list is terminated with a terminating <b>NULL</b> character. For example, a list of two names could be: 




L"<i>first</i>.dll\0" L"<i>second</i>.dll\0" L"\0"

To retrieve the number of wide characters the buffer must hold, this parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcchDllList [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in wide characters, of the returned list pointed to by the <i>pwszDllList</i> parameter. When the function returns, the variable pointed to by the <i>pcchDllList</i> parameter contains the number of wide characters stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

This function has the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pwszDllList</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in wide characters, in the variable pointed to by <i>pcchDllList</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">OID Support Functions</a>
 

 

