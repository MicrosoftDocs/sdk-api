---
UID: NF:ncrypt.NCryptEnumAlgorithms
title: NCryptEnumAlgorithms function
author: windows-sdk-content
description: Obtains the names of the algorithms that are supported by the specified key storage provider.
old-location: security\ncryptenumalgorithms_func.htm
old-project: SecCNG
ms.assetid: ea4f270b-c556-4f52-892a-199c9cfced26
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, NCRYPT_CIPHER_OPERATION, NCRYPT_HASH_OPERATION, NCRYPT_SECRET_AGREEMENT_OPERATION, NCRYPT_SIGNATURE_OPERATION, NCRYPT_SILENT_FLAG, NCryptEnumAlgorithms, NCryptEnumAlgorithms function [Security], ncrypt/NCryptEnumAlgorithms, security.ncryptenumalgorithms_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ncrypt.dll
api_name:
-	NCryptEnumAlgorithms
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NCryptEnumAlgorithms function


## -description


The <b>NCryptEnumAlgorithms</b> function obtains the names of the algorithms that are supported by the specified key storage provider.


## -parameters




### -param hProvider [in]

The handle of the key storage provider to enumerate the algorithms for. This handle is obtained with the <a href="https://msdn.microsoft.com/febcf440-78b3-420b-b13d-030e8071cd50">NCryptOpenStorageProvider</a> function.


### -param dwAlgOperations [in]

A set of values that determine which algorithm classes to enumerate. This can be zero or a combination of one or more of the following values. If <i>dwAlgOperations</i> is zero, all algorithms are enumerated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_CIPHER_OPERATION"></a><a id="ncrypt_cipher_operation"></a><dl>
<dt><b>NCRYPT_CIPHER_OPERATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enumerate the cipher (symmetric encryption) algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_HASH_OPERATION"></a><a id="ncrypt_hash_operation"></a><dl>
<dt><b>NCRYPT_HASH_OPERATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enumerate the hashing algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION"></a><a id="ncrypt_asymmetric_encryption_operation"></a><dl>
<dt><b>NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enumerate the asymmetric encryption algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SECRET_AGREEMENT_OPERATION"></a><a id="ncrypt_secret_agreement_operation"></a><dl>
<dt><b>NCRYPT_SECRET_AGREEMENT_OPERATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Enumerate the secret agreement algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SIGNATURE_OPERATION"></a><a id="ncrypt_signature_operation"></a><dl>
<dt><b>NCRYPT_SIGNATURE_OPERATION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Enumerate the digital signature algorithms.

</td>
</tr>
</table>
 


### -param pdwAlgCount [out]

The address of a <b>DWORD</b> that receives the number of elements in the <i>ppAlgList</i> array.


### -param ppAlgList [out]

The address of an <a href="https://msdn.microsoft.com/79b0193e-3be8-46ce-a422-40ed9698363f">NCryptAlgorithmName</a> structure pointer that receives an array of the registered algorithm names. The variable pointed to by the <i>pdwAlgCount</i> parameter receives the number of elements in this array.

When this memory is no longer needed, it must be freed by passing this pointer to the <a href="https://msdn.microsoft.com/15f19999-cf64-4a30-b38d-9372066add0a">NCryptFreeBuffer</a> function.


### -param dwFlags [in]

Flags that modify function behavior. This can be zero (0) or the following value.

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
Requests that the key service provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



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
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProvider</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



