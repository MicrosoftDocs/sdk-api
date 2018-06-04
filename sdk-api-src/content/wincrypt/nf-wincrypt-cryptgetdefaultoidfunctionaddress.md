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

# CryptGetDefaultOIDFunctionAddress function


## -description


The <b>CryptGetDefaultOIDFunctionAddress</b> function loads the DLL that contains a default function address. It can also return the address of the first or next installed default <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) function in an initialized function set and load the DLL that contains the address  of that function.


## -parameters




### -param hFuncSet [in]

Function set handle previously obtained from a call to 
<a href="https://msdn.microsoft.com/576a2989-ed7f-417d-b60e-24baf90a6554">CryptInitOIDFunctionSet</a>.


### -param dwEncodingType [in]

Encoding type to be matched. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. To match both current encoding types, use:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING


### -param pwszDll [in, optional]

Name of the DLL to load. Normally, the DLL name is obtained from the list returned by 
<a href="https://msdn.microsoft.com/9d4643c8-a582-4c19-bd77-33b94e953818">CryptGetDefaultOIDDllList</a>. If <i>pwszDll</i> is <b>NULL</b>, a search is performed on the list of installed default functions.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param ppvFuncAddr [out]

A pointer to the address of the return function. If the function fails, a <b>NULL</b> is returned in <i>ppvFuncAddr</i>.


### -param phFuncAddr [in, out]

Used only if <i>pwszDll</i> is <b>NULL</b>. On the first call to the function, *<i>phFuncAddr</i> must be <b>NULL</b> to acquire the first installed function. 




When this function is successful, *<i>phFuncAddr</i> is set to a function handle. The <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> for the function handle is incremented.

After the first call to the function, <i>phFuncAddr</i> is set to the pointer returned by the previous call. This input pointer is always freed within the function through a call to 
<a href="https://msdn.microsoft.com/cacacff3-25b7-4ed4-885b-b4b0b326628f">CryptFreeOIDFunctionAddress</a> by this function. The call to free the pointer is always made even when the main function returns an error.

A non-<b>NULL</b><i>phFuncAddr</i> must be released either through a call to <a href="https://msdn.microsoft.com/cacacff3-25b7-4ed4-885b-b4b0b326628f">CryptFreeOIDFunctionAddress</a> or by being passed back as input to this function or as input to 
<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a>.

If <i>pwszDll</i> is not <b>NULL</b>, the value of this parameter is ignored and a non-<b>NULL</b> pointer is not freed.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).





## -see-also




<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

