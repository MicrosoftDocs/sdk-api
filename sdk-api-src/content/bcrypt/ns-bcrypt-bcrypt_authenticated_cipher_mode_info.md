---
UID: NS:bcrypt._BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
title: BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO (bcrypt.h)
description: Used with the BCryptEncrypt and BCryptDecrypt functions to contain additional information related to authenticated cipher modes.
helpviewer_keywords: ["*PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO","BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO","BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure [Security]","BCRYPT_AUTH_MODE_CHAIN_CALLS_FLAG","BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG","BCryptDecrypt","BCryptEncrypt","PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO","PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure pointer [Security]","bcrypt/BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO","bcrypt/PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO","security.bcrypt_authenticated_cipher_mode_info"]
old-location: security\bcrypt_authenticated_cipher_mode_info.htm
tech.root: security
ms.assetid: 6c00f458-7198-44fe-bdb6-2c2eb9995bd9
ms.date: 12/05/2018
ms.keywords: '*PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure [Security], BCRYPT_AUTH_MODE_CHAIN_CALLS_FLAG, BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG, BCryptDecrypt, BCryptEncrypt, PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure pointer [Security], bcrypt/BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, bcrypt/PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, security.bcrypt_authenticated_cipher_mode_info'
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO, *PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
 - bcrypt/_BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
 - PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
 - bcrypt/PBCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
 - BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
 - bcrypt/BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO
---

# BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure


## -description

The <b>BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</b> structure is used with the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> functions to contain additional information related to authenticated cipher modes.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure. Do not set this field directly. Use the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypt_init_auth_mode_info">BCRYPT_INIT_AUTH_MODE_INFO</a> macro instead.

### -field dwInfoVersion

The version number of the structure.   The only supported value is <b>BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO_VERSION</b>. Do not set this field directly. Use the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypt_init_auth_mode_info">BCRYPT_INIT_AUTH_MODE_INFO</a> macro instead.

### -field pbNonce

A pointer to a buffer that contains a nonce. The Microsoft algorithm providers for <a href="/windows/desktop/SecGloss/a-gly">Advanced Encryption Standard</a> (AES) require a nonce for the Counter with CBC-MAC (CCM) and Galois/Counter Mode (GCM) chaining modes, and will return an error if none is present. If a nonce is not used, this member must be set to <b>NULL</b>.

### -field cbNonce

The size, in bytes, of the buffer pointed to by the <b>pbNonce</b> member.
	If a nonce is not used, this member must be set to zero.

### -field pbAuthData

A pointer to a buffer that contains the authenticated data.  This is data that will be included in the <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) but not encrypted.  If there is no authenticated data, this member must be set to <b>NULL</b>.

### -field cbAuthData

The size, in bytes, of the buffer pointed to by the <b>pbAuthData</b> member.  If there is no authenticated data, this member must be set to zero.

### -field pbTag

A pointer to a buffer.

The use of this member depends on the function to which the structure is passed.

<table>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="BCryptEncrypt"></a><a id="bcryptencrypt"></a><a id="BCRYPTENCRYPT"></a><dl>
<dt><b><a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The  buffer will receive the authentication tag.

</td>
</tr>
<tr>
<td width="40%"><a id="BCryptDecrypt"></a><a id="bcryptdecrypt"></a><a id="BCRYPTDECRYPT"></a><dl>
<dt><b><a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The buffer contains the authentication tag to be checked against.

</td>
</tr>
</table>
 

If there is no tag, this member must be set to <b>NULL</b>.

### -field cbTag

The size, in bytes, of the <b>pbTag</b> buffer. The buffer must be long enough to include the whole authentication tag.  Some authentication modes, such as CCM and GCM, support checking against a tag with multiple lengths.  To obtain the valid authentication tag lengths use <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> to query the <b>BCRYPT_AUTH_TAG_LENGTH</b> property.  If there is no tag, this member must be set to zero.

### -field pbMacContext

A pointer to a buffer that stores the partially computed MAC between calls to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> when chaining encryption or decryption.

If the input to encryption or decryption is scattered across multiple buffers, then you must chain calls to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> functions. Chaining is indicated by setting the <b>BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG</b> flag in the <b>dwFlags</b> member.

This buffer must be supplied by the caller and must be at least as large as the maximum length of an authentication tag for the cipher you are using. To get the valid authentication tag lengths, use <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> to query the <b>BCRYPT_AUTH_TAG_LENGTH</b> property.

If <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and  <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> calls are not being chained, this member must be set to <b>NULL</b>.

### -field cbMacContext

The size, in bytes, of the buffer pointed to by the <b>pbMacContext</b> member.  If <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and  <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> calls are not being chained, this member must be set to zero.

### -field cbAAD

The length, in bytes, of additional authenticated data (AAD) to be used by the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> functions.  This member is used only  when chaining calls.

This member is used only when the <b>BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG</b> flag in the <b>dwFlags</b> member is set.

On the first call to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> you must set this field to zero.


<div class="alert"><b>Note</b>  During the chaining sequence, this member is maintained internally and must not be changed or the value of the computed MAC will be corrupted.</div>
<div> </div>

### -field cbData

The length, in bytes, of the payload data that was encrypted or decrypted.  This member is used only when chaining calls.

This member is used only when the <b>BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG</b> flag in the <b>dwFlags</b> member is set.

On the first call to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> you must set this field to zero, , either directly or by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypt_init_auth_mode_info">BCRYPT_INIT_AUTH_INFO</a> macro


<div class="alert"><b>Note</b>  During the chaining sequence, this member is maintained internally and must not be changed or the value of the computed MAC will be corrupted.</div>
<div> </div>

### -field dwFlags

This flag is used when chaining <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> function calls.  If calls are not being chained, this member must be set to zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
For <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>, calculate the authentication tag and place it in the buffer pointed to by the <b>pbTag</b> member. 

For <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a>, calculate the authentication tag and compare it against the tag passed in to the buffer pointed to by the <b>pbTag</b> member. When chaining multiple calls to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> or <b>BCryptDecrypt</b>, this value signals the end of the chain.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_AUTH_MODE_CHAIN_CALLS_FLAG"></a><a id="bcrypt_auth_mode_chain_calls_flag"></a><dl>
<dt><b>BCRYPT_AUTH_MODE_CHAIN_CALLS_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> function calls are being chained and that the MAC value will not be computed. On the last call in the chain, clear this value to compute the MAC value for the entire chain.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG"></a><a id="bcrypt_auth_mode_in_progress_flag"></a><dl>
<dt><b>BCRYPT_AUTH_MODE_IN_PROGRESS_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates that this <b>BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</b> structure is being used in a sequence of chained <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdecrypt">BCryptDecrypt</a> function calls. This flag is set and maintained internally.


<div class="alert"><b>Note</b>  During the chaining sequence, this flag value is maintained internally and must not be changed or the value of the computed MAC will be corrupted.</div>
<div> </div>


</td>
</tr>
</table>

## -remarks

The size of this structure is different between 64-bit and 32-bit operating systems.  On 64-bit operating systems, the size is different between 64-bit and 32-bit processes.  Instances of this structure must not be shared across threads or passed between processes.