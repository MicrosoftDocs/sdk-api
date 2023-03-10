---
UID: NF:ncrypt.NCryptVerifySignature
title: NCryptVerifySignature function (ncrypt.h)
description: Verifies that the specified signature matches the specified hash. (NCryptVerifySignature)
helpviewer_keywords: ["NCRYPT_PAD_PKCS1_FLAG","NCRYPT_PAD_PSS_FLAG","NCRYPT_SILENT_FLAG","NCryptVerifySignature","NCryptVerifySignature function [Security]","ncrypt/NCryptVerifySignature","security.ncryptverifysignature_func"]
old-location: security\ncryptverifysignature_func.htm
tech.root: security
ms.assetid: 9a839d99-4e9a-4114-982c-51dee38d2949
ms.date: 12/05/2018
ms.keywords: NCRYPT_PAD_PKCS1_FLAG, NCRYPT_PAD_PSS_FLAG, NCRYPT_SILENT_FLAG, NCryptVerifySignature, NCryptVerifySignature function [Security], ncrypt/NCryptVerifySignature, security.ncryptverifysignature_func
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
 - NCryptVerifySignature
 - ncrypt/NCryptVerifySignature
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
 - NCryptVerifySignature
---

# NCryptVerifySignature function


## -description

The <b>NCryptVerifySignature</b> function verifies that the specified signature matches the specified hash.

## -parameters

### -param hKey [in]

The handle of the key to use to decrypt the signature. This must be an identical key or the public key portion of the key pair used to sign the data with the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a> function.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the <i>dwFlags</i> parameter. This parameter is only used with asymmetric keys and must be <b>NULL</b> otherwise.

### -param pbHashValue [in]

The address of a buffer that contains the hash of the data. The <i>cbHash</i> parameter contains the size of this buffer.

### -param cbHashValue [in]

The size, in bytes, of the <i>pbHash</i> buffer.

### -param pbSignature [in]

The address of a buffer that contains the signed hash of the data. The <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a> function is used to create the signature. The <i>cbSignature</i> parameter contains the size of this buffer.

### -param cbSignature [in]

The size, in bytes, of the <i>pbSignature</i> buffer. The <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a> function is used to create the signature.

### -param dwFlags [in]

Flags that modify function behavior. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.

If the key is a symmetric key, this parameter is not used and should be zero.


If the key is an asymmetric key, this can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PAD_PKCS1_FLAG"></a><a id="ncrypt_pad_pkcs1_flag"></a><dl>
<dt><b>NCRYPT_PAD_PKCS1_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The PKCS1 padding scheme was used when the signature was created. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pkcs1_padding_info">BCRYPT_PKCS1_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PAD_PSS_FLAG"></a><a id="ncrypt_pad_pss_flag"></a><dl>
<dt><b>NCRYPT_PAD_PSS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The Probabilistic Signature Scheme (PSS) padding scheme was used when the signature was created. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pss_padding_info">BCRYPT_PSS_PADDING_INFO</a> structure.

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
<dt><b>NTE_BAD_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The signature was not verified.

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
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider used to create the key handle specified by the <i>hKey</i> parameter is not a signing algorithm.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a>
