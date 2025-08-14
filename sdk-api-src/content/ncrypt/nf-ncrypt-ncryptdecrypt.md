---
UID: NF:ncrypt.NCryptDecrypt
title: NCryptDecrypt function (ncrypt.h)
description: Decrypts a block of encrypted data.
helpviewer_keywords: ["NCRYPT_NO_PADDING_FLAG","NCRYPT_PAD_OAEP_FLAG","NCRYPT_PAD_PKCS1_FLAG","NCRYPT_SILENT_FLAG","NCryptDecrypt","NCryptDecrypt function [Security]","ncrypt/NCryptDecrypt","security.ncryptdecrypt_func"]
old-location: security\ncryptdecrypt_func.htm
tech.root: security
ms.assetid: 02c309bc-8c94-4c0f-901f-e024c83c824a
ms.date: 12/05/2018
ms.keywords: NCRYPT_NO_PADDING_FLAG, NCRYPT_PAD_OAEP_FLAG, NCRYPT_PAD_PKCS1_FLAG, NCRYPT_SILENT_FLAG, NCryptDecrypt, NCryptDecrypt function [Security], ncrypt/NCryptDecrypt, security.ncryptdecrypt_func
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
 - NCryptDecrypt
 - ncrypt/NCryptDecrypt
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
 - NCryptDecrypt
---

# NCryptDecrypt function


## -description

The <b>NCryptDecrypt</b> function decrypts a block of encrypted data.

## -parameters

### -param hKey [in]

The handle of the key to use to decrypt the data.

### -param pbInput [in]

The address of a buffer that contains the data to be decrypted. The <i>cbInput</i> parameter contains the size of the data to decrypt. For more information, see Remarks.

### -param cbInput [in]

The number of bytes in the <i>pbInput</i> buffer to decrypt.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the <i>dwFlags</i> parameter. This parameter is only used with asymmetric keys and must be <b>NULL</b> otherwise.

### -param pbOutput [out]

The address of a buffer that will receive the decrypted data produced by this function. The <i>cbOutput</i> parameter contains the size of this buffer. For more information, see Remarks.

If this parameter is <b>NULL</b>, this function will calculate the size needed for the decrypted data and return the size in the location pointed to by the <i>pcbResult</i> parameter.

### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer. This parameter is ignored if the <i>pbOutput</i> parameter is <b>NULL</b>.

### -param pcbResult [out]

A pointer to a <b>DWORD</b> variable that receives the number of bytes copied to the <i>pbOutput</i> buffer. If <i>pbOutput</i> is <b>NULL</b>, this receives the size, in bytes, required for the decrypted data.

### -param dwFlags [in]

Flags that modify function behavior. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.


If the key is an asymmetric key, this can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_NO_PADDING_FLAG"></a><a id="ncrypt_no_padding_flag"></a><dl>
<dt><b>NCRYPT_NO_PADDING_FLAG</b></dt>
</dl>
</td>
<td width="60%">
No padding was used when the data was encrypted. The <i>pPaddingInfo</i> parameter is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PAD_OAEP_FLAG"></a><a id="ncrypt_pad_oaep_flag"></a><dl>
<dt><b>NCRYPT_PAD_OAEP_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The Optimal Asymmetric Encryption Padding (OAEP) scheme was used when the data was encrypted. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oaep_padding_info">BCRYPT_OAEP_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PAD_PKCS1_FLAG"></a><a id="ncrypt_pad_pkcs1_flag"></a><dl>
<dt><b>NCRYPT_PAD_PKCS1_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The data was padded with a random number to round out the block size when the data was encrypted. The <i>pPaddingInfo</i> parameter is not used.

</td>
</tr>
</table>
 

The following value can be used for any key.

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
Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

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
<dt><b>NTE_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by the <i>cbOutput</i> parameter is not large enough to hold the decrypted data.

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
<dt><b>NTE_PERM</b></dt>
</dl>
</td>
<td width="60%">
The key identified by the <i>hKey</i> parameter cannot be used for decryption.

</td>
</tr>
</table>

## -remarks

The <i>pbInput</i> and <i>pbOutput</i> parameters can point to the same buffer. In this case, this function will perform the decryption in place.

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptencrypt">NCryptEncrypt</a>