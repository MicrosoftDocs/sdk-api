---
UID: NF:ncrypt.NCryptSignHash
title: NCryptSignHash function (ncrypt.h)
description: Creates a signature of a hash value. (NCryptSignHash)
helpviewer_keywords: ["BCRYPT_PAD_PKCS1","BCRYPT_PAD_PSS","NCRYPT_SILENT_FLAG","NCryptSignHash","NCryptSignHash function [Security]","ncrypt/NCryptSignHash","security.ncryptsignhash_func"]
old-location: security\ncryptsignhash_func.htm
tech.root: security
ms.assetid: 7404e37a-d7c6-49ed-b951-6081dd2b921a
ms.date: 12/05/2018
ms.keywords: BCRYPT_PAD_PKCS1, BCRYPT_PAD_PSS, NCRYPT_SILENT_FLAG, NCryptSignHash, NCryptSignHash function [Security], ncrypt/NCryptSignHash, security.ncryptsignhash_func
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptSignHash
 - ncrypt/NCryptSignHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptSignHash
---

# NCryptSignHash function


## -description

The <b>NCryptSignHash</b> function creates a signature of a hash value.

## -parameters

### -param hKey [in]

The handle of the key to use to sign the hash.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the <i>dwFlags</i> parameter. This parameter is only used with asymmetric keys and must be <b>NULL</b> otherwise.

### -param pbHashValue [in]

A pointer to a buffer that contains the hash value to sign. The <i>cbInput</i> parameter contains the size of this buffer.

### -param cbHashValue [in]

The number of bytes in the <i>pbHashValue</i> buffer to sign.

### -param pbSignature [out]

The address of a buffer to receive the signature produced by this function. The <i>cbSignature</i> parameter contains the size of this buffer.

If this parameter is <b>NULL</b>, this function will calculate the size required for the signature and return the size in the location pointed to by the <i>pcbResult</i> parameter.

### -param cbSignature [in]

The size, in bytes, of the <i>pbSignature</i> buffer. This parameter is ignored if the <i>pbSignature</i> parameter is <b>NULL</b>.

### -param pcbResult [out]

A pointer to a <b>DWORD</b> variable that receives the number of bytes copied to the <i>pbSignature</i> buffer. 

If <i>pbSignature</i> is <b>NULL</b>, this receives the size, in bytes, required for the signature.

### -param dwFlags [in]

Flags that modify function behavior. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.

If the key is a symmetric key, this parameter is not used and should be set to zero.


If the key is an asymmetric key, this can be one of the following values.



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
Use the PKCS1 padding scheme. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pkcs1_padding_info">BCRYPT_PKCS1_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PSS"></a><a id="bcrypt_pad_pss"></a><dl>
<dt><b>BCRYPT_PAD_PSS</b></dt>
</dl>
</td>
<td width="60%">
Use the Probabilistic Signature Scheme (PSS) padding scheme. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pss_padding_info">BCRYPT_PSS_PADDING_INFO</a> structure.

</td>
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
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The key represented by the <i>hKey</i> parameter does not support signing.

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
The <i>hKey</i> parameter is not valid.

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

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.
