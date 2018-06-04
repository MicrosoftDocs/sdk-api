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

# CryptCATAdminAcquireContext2 function


## -description


The <b>CryptCATAdminAcquireContext2</b> function acquires a handle to a catalog administrator context for a given hash algorithm and hash policy.

 You can use this handle in subsequent calls to the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>
</li>
<li>
<a href="https://msdn.microsoft.com/33ab2d01-94ab-4d23-a054-9da0731485d6">CryptCATAdminEnumCatalogFromHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e09fe991-0e7a-45da-910a-8cb148bdff9a">CryptCATAdminRemoveCatalog</a>
</li>
</ul>This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param phCatAdmin [out]

A pointer to the catalog administrator context handle that is assigned by this function. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/dff253dc-c444-46be-a383-41340d634cce">CryptCATAdminReleaseContext</a> function.


### -param pgSubsystem [in, optional]

A pointer to the <b>GUID</b> that identifies the subsystem. DRIVER_ACTION_VERIFY represents the subsystem for operating system components and third party drivers. This is the subsystem used by most implementations.


### -param pwszHashAlgorithm [in, optional]

Optional null-terminated Unicode string that specifies the name of the hash algorithm to use when calculating and verifying hashes. This value can be <b>NULL</b>. If it is <b>NULL</b>, the default hashing algorithm may be chosen, depending on the value you set for the <i>pStrongHashPolicy</i> parameter. The default algorithm in Windows 8 is SHA1. The default may change in future Windows versions. For more information, see Remarks.


### -param pStrongHashPolicy [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure that contains the parameters used to check for strong signatures. The function chooses the lowest common hashing algorithm that satisfies the specified policy and the algorithm specified by the <i>pwszHashAlgorithm</i> parameter or the system default algorithm (if no algorithm is specified).


### -param dwFlags

Reserved. This value must be zero.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>phCatAdmin</i> parameter cannot be <b>NULL</b>.

The <i>dwFlags</i> parameter must be zero (0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to create a new catalog administrator object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The hash algorithm specified by the <i>pwszHashAlgorithm</i> parameter cannot be found.

</td>
</tr>
</table>
 




## -remarks



This function enables you to choose, or chooses for you, the hash algorithm to be used in  functions that require the catalog administrator context. Although you can set the name of the hashing algorithm, we recommend that you let the function determine the algorithm. Doing so protects your application from hard coding algorithms that may become untrusted in the future.




## -see-also




<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>



<a href="https://msdn.microsoft.com/dff253dc-c444-46be-a383-41340d634cce">CryptCATAdminReleaseContext</a>



<a href="https://msdn.microsoft.com/e09fe991-0e7a-45da-910a-8cb148bdff9a">CryptCATAdminRemoveCatalog</a>
 

 

