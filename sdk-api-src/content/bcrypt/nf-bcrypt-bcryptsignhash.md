---
UID: NF:bcrypt.BCryptSignHash
title: BCryptSignHash function
author: windows-driver-content
description: Creates a signature of a hash value.
old-location: security\bcryptsignhash_func.htm
old-project: SecCNG
ms.assetid: f402ea9e-89ae-4ccc-9591-aa2328287c0e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: BCRYPT_PAD_PKCS1, BCRYPT_PAD_PSS, BCryptSignHash, BCryptSignHash function [Security], bcrypt/BCryptSignHash, security.bcryptsignhash_func
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bcrypt.h
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
req.typenames: HASHALGORITHM_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bcrypt.dll
-	Ksecdd.sys
api_name:
-	BCryptSignHash
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptSignHash function


## -description


The <b>BCryptSignHash</b> function creates a signature of a hash value.


## -parameters




### -param hKey [in]

The handle of the key to use to sign the hash.


### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the <i>dwFlags</i> parameter. This parameter is only used with asymmetric keys and must be <b>NULL</b> otherwise.


### -param pbInput [in]

A pointer to a buffer that contains the hash value to sign. The <i>cbInput</i> parameter contains the size of this buffer.


### -param cbInput [in]

The number of bytes in the <i>pbInput</i> buffer to sign.


### -param pbOutput [out]

The address of a buffer to receive the signature produced by this function. The <i>cbOutput</i> parameter contains the size of this buffer.

If this parameter is <b>NULL</b>, this function will calculate the size required for the signature and return the size in the location pointed to by the <i>pcbResult</i> parameter.


### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer. This parameter is ignored if the <i>pbOutput</i> parameter is <b>NULL</b>.


### -param pcbResult [out]

A pointer to a <b>ULONG</b> variable that receives the number of bytes copied to the <i>pbOutput</i> buffer. 

If <i>pbOutput</i> is <b>NULL</b>, this receives the size, in bytes, required for the signature.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.


This can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PKCS1"></a><a id="bcrypt_pad_pkcs1"></a><dl>
<dt><b>BCRYPT_PAD_PKCS1</b></dt>
</dl>
</td>
<td width="60%">
Use the PKCS1 padding scheme. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/920fa461-5b7e-4429-972d-e7c83fb62c64">BCRYPT_PKCS1_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PSS"></a><a id="bcrypt_pad_pss"></a><dl>
<dt><b>BCRYPT_PAD_PSS</b></dt>
</dl>
</td>
<td width="60%">
Use the Probabilistic Signature Scheme (PSS) padding scheme. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="https://msdn.microsoft.com/28605b34-b1e1-4460-a8f0-b0fe9f9b94d4">BCRYPT_PSS_PADDING_INFO</a> structure.

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
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The key handle specified by the <i>hKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider used to create the key handle specified by the <i>hKey</i> parameter is not a signing algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The memory size specified by the <i>cbOutput</i> parameter is not large enough to hold the signature.

</td>
</tr>
</table>
 




## -remarks



This function will encrypt the hash value with the specified key to create the signature.

To later verify that the signature is valid, call the <a href="https://msdn.microsoft.com/95c32056-e444-441c-bbc1-c5ae82aba964">BCryptVerifySignature</a> function with an identical key and an identical hash of the original data.

Depending on what processor modes a provider supports, <b>BCryptSignHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptSignHash</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/95c32056-e444-441c-bbc1-c5ae82aba964">BCryptVerifySignature</a>
 

 

