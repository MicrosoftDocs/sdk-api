---
UID: NF:ncryptprotect.NCryptProtectSecret
title: NCryptProtectSecret function
author: windows-sdk-content
description: Encrypts data to a specified protection descriptor.
old-location: security\ncryptprotectsecret.htm
tech.root: seccng
ms.assetid: 8726F92B-34D5-4696-8803-3D7F50F1006D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptProtectSecret, NCryptProtectSecret function [Security], ncryptprotect/NCryptProtectSecret, security.ncryptprotectsecret
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptProtectSecret
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptProtectSecret function


## -description


The <b>NCryptProtectSecret</b> function encrypts data to a specified protection descriptor. Call <a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a> to decrypt the data.


## -parameters




### -param hDescriptor [in]

Handle of the protection descriptor object. Create the handle by calling <a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>.


### -param dwFlags [in]

The flag can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider not display a user interface.

</td>
</tr>
</table>
 


### -param pbData [in]

Pointer to the byte array to be protected.


### -param cbData [in]

Number of bytes in the binary array specified by the <i>pbData</i> parameter.


### -param pMemPara [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/4F546F51-E4DE-4703-B1D1-F84165C3C31B">NCRYPT_ALLOC_PARA</a> structure that you can use to specify custom memory management functions. If you set this argument to <b>NULL</b>, the <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function is used internally to allocate memory and your application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release memory pointed to by the <i>ppbProtectedBlob</i> parameter.


### -param hWnd [in, optional]

Handle to the parent window of the user interface, if any, to be displayed.


### -param ppbProtectedBlob [out]

Address of a variable that receives a pointer to the encrypted data.


### -param pcbProtectedBlob [out]

Pointer to a <b>ULONG</b> variable that contains the size, in bytes, of the encrypted data pointed to by the <i>ppbProtectedBlob</i> variable.


## -returns



Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbData</i>, <i>ppbProtectedBlob</i>, and <i>pcbProtectedBlob</i> parameters cannot be <b>NULL</b>.

The <i>cbData</i> parameter cannot be less than one.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to allocate the content encryption key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hDescriptor</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



Use the <b>NCryptProtectSecret</b> function to protect keys, key material, and passwords. Use the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> and the <a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a> functions to encrypt larger messages.




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>



<a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>
 

 

