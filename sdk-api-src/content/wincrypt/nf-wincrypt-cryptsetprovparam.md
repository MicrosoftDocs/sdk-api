---
UID: NF:wincrypt.CryptSetProvParam
title: CryptSetProvParam function
author: windows-sdk-content
description: Customizes the operations of a cryptographic service provider (CSP). This function is commonly used to set a security descriptor on the key container associated with a CSP to control access to the private keys in that key container.
old-location: security\cryptsetprovparam.htm
tech.root: seccrypto
ms.assetid: 98306a7b-b218-4eb4-99f0-0b5bcc632a13
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CryptSetProvParam, CryptSetProvParam function [Security], PP_CLIENT_HWND, PP_DELETEKEY, PP_KEYEXCHANGE_ALG, PP_KEYEXCHANGE_KEYSIZE, PP_KEYEXCHANGE_PIN, PP_KEYSET_SEC_DESCR, PP_PIN_PROMPT_STRING, PP_ROOT_CERTSTORE, PP_SECURE_KEYEXCHANGE_PIN, PP_SECURE_SIGNATURE_PIN, PP_SIGNATURE_ALG, PP_SIGNATURE_KEYSIZE, PP_SIGNATURE_PIN, PP_SMARTCARD_GUID, PP_SMARTCARD_READER, PP_UI_PROMPT, PP_USER_CERTSTORE, PP_USE_HARDWARE_RNG, _crypto2_cryptsetprovparam, security.cryptsetprovparam, wincrypt/CryptSetProvParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptSetProvParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSetProvParam function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetProvParam</b> function customizes the operations of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This function is commonly used to set a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> on the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> associated with a CSP to control access to the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a> in that key container.


## -parameters




### -param hProv [in]

The handle of a CSP for which to set values. This handle must have already been created by using 
the <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function.


### -param dwParam [in]

Specifies the parameter to set. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PP_CLIENT_HWND"></a><a id="pp_client_hwnd"></a><dl>
<dt><b>PP_CLIENT_HWND</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Set the window handle that the provider uses as the parent of any dialog boxes it creates. <i>pbData</i> contains a pointer to an <b>HWND</b> that contains the parent window handle.

This parameter must be set before calling 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> because many CSPs will display a user interface when <b>CryptAcquireContext</b> is called. You can pass <b>NULL</b> for the <i>hProv</i> parameter to set this window handle for all cryptographic contexts subsequently acquired within this <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_DELETEKEY"></a><a id="pp_deletekey"></a><dl>
<dt><b>PP_DELETEKEY</b></dt>
<dt>24 (0x18)</dt>
</dl>
</td>
<td width="60%">
Delete the ephemeral key associated with a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>, <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encryption</a>, or verification context. This will free memory and clear registry settings associated with the key.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYEXCHANGE_ALG"></a><a id="pp_keyexchange_alg"></a><dl>
<dt><b>PP_KEYEXCHANGE_ALG</b></dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYEXCHANGE_PIN"></a><a id="pp_keyexchange_pin"></a><dl>
<dt><b>PP_KEYEXCHANGE_PIN</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
Specifies that the key exchange PIN is contained in <i>pbData</i>. The PIN is represented as a null-terminated ASCII string.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYEXCHANGE_KEYSIZE"></a><a id="pp_keyexchange_keysize"></a><dl>
<dt><b>PP_KEYEXCHANGE_KEYSIZE</b></dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_KEYSET_SEC_DESCR"></a><a id="pp_keyset_sec_descr"></a><dl>
<dt><b>PP_KEYSET_SEC_DESCR</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
Sets the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> on the key storage container. The <i>pbData</i> parameter is the address of a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the new security descriptor for the key storage container.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_PIN_PROMPT_STRING"></a><a id="pp_pin_prompt_string"></a><dl>
<dt><b>PP_PIN_PROMPT_STRING</b></dt>
<dt>44 (0x2C)</dt>
</dl>
</td>
<td width="60%">
Sets an alternate prompt string to display to the user when the user's PIN is requested. The <i>pbData</i> parameter  is a pointer to a null-terminated Unicode string.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_ROOT_CERTSTORE"></a><a id="pp_root_certstore"></a><dl>
<dt><b>PP_ROOT_CERTSTORE</b></dt>
<dt>46 (0x2E)</dt>
</dl>
</td>
<td width="60%">
Sets the root certificate store for the smart card.  The provider will copy the root certificates from this store onto the smart card.

The <i>pbData</i> parameter is an <b>HCERTSTORE</b> variable that contains the handle of the new certificate store. The provider will copy the certificates from the store during this call, so it is safe to close this store after this function is called.

<b>Windows XP and Windows Server 2003:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SIGNATURE_ALG"></a><a id="pp_signature_alg"></a><dl>
<dt><b>PP_SIGNATURE_ALG</b></dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SIGNATURE_PIN"></a><a id="pp_signature_pin"></a><dl>
<dt><b>PP_SIGNATURE_PIN</b></dt>
<dt>33 (0x21)</dt>
</dl>
</td>
<td width="60%">
Specifies the signature PIN. The <i>pbData</i> parameter is a null-terminated ASCII string that represents the PIN.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SIGNATURE_KEYSIZE"></a><a id="pp_signature_keysize"></a><dl>
<dt><b>PP_SIGNATURE_KEYSIZE</b></dt>
</dl>
</td>
<td width="60%">
This constant is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_UI_PROMPT"></a><a id="pp_ui_prompt"></a><dl>
<dt><b>PP_UI_PROMPT</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">
For a smart card provider, sets the search string that is displayed to the user as a prompt to insert the smart card. This string is passed as the <b>lpstrSearchDesc</b> member of the <a href="https://msdn.microsoft.com/fb9e64a9-441a-4c7b-b404-79682778c694">OPENCARDNAME_EX</a> structure that is passed to the <a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> function. This string is used for the lifetime of the calling process.

The <i>pbData</i> parameter is a pointer to a null-terminated Unicode string.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_USE_HARDWARE_RNG"></a><a id="pp_use_hardware_rng"></a><dl>
<dt><b>PP_USE_HARDWARE_RNG</b></dt>
<dt>38 (0x26)</dt>
</dl>
</td>
<td width="60%">
Specifies that the CSP must exclusively use the hardware random number generator (RNG). When <b>PP_USE_HARDWARE_RNG</b> is set, random values are taken exclusively from the hardware RNG and no other sources are used. If a hardware RNG is supported by the CSP and it can be exclusively used, the function succeeds and returns <b>TRUE</b>; otherwise, the function fails and returns <b>FALSE</b>. The <i>pbData</i> parameter must be <b>NULL</b> and <i>dwFlags</i> must be zero when using this value.

None of the Microsoft CSPs currently support using a hardware RNG.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_USER_CERTSTORE"></a><a id="pp_user_certstore"></a><dl>
<dt><b>PP_USER_CERTSTORE</b></dt>
<dt>42 (0x2A)</dt>
</dl>
</td>
<td width="60%">
Specifies the user certificate store for the smart card. This certificate store contains all of the user certificates that are stored on the smart card. The certificates in this store are encoded by using PKCS_7_ASN_ENCODING or X509_ASN_ENCODING encoding and should contain the <b>CERT_KEY_PROV_INFO_PROP_ID</b> property. 

The <i>pbData</i> parameter is an <b>HCERTSTORE</b> variable that receives the handle of an in-memory certificate store. When this handle is no longer needed, the caller must close it by using the <a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> function.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SECURE_KEYEXCHANGE_PIN"></a><a id="pp_secure_keyexchange_pin"></a><dl>
<dt><b>PP_SECURE_KEYEXCHANGE_PIN</b></dt>
<dt>47 (0x2F)</dt>
</dl>
</td>
<td width="60%">
Specifies that an encrypted key exchange PIN is contained in <i>pbData</i>. The <i>pbData</i> parameter contains a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SECURE_SIGNATURE_PIN"></a><a id="pp_secure_signature_pin"></a><dl>
<dt><b>PP_SECURE_SIGNATURE_PIN</b></dt>
<dt>48 (0x30)</dt>
</dl>
</td>
<td width="60%">
Specifies that an encrypted signature PIN is contained in <i>pbData</i>. The <i>pbData</i> parameter contains a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SMARTCARD_READER"></a><a id="pp_smartcard_reader"></a><dl>
<dt><b>PP_SMARTCARD_READER</b></dt>
<dt>43 (0x2B)</dt>
</dl>
</td>
<td width="60%">
Specifies the name of the smart card reader. The <i>pbData</i> parameter is the address of an ANSI character array that contains a null-terminated ANSI string that contains the name of the smart card reader. 

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PP_SMARTCARD_GUID_"></a><a id="pp_smartcard_guid_"></a><dl>
<dt><b>PP_SMARTCARD_GUID </b></dt>
<dt>45 (0x2D)</dt>
</dl>
</td>
<td width="60%">
Specifies the identifier of the smart card. The <i>pbData</i> parameter is the address of a <b>GUID</b> structure that contains the identifier of the smart card.

<b>Windows Server 2003 and Windows XP:  </b>This parameter is not supported.

</td>
</tr>
</table>
 


### -param pbData [in]

A pointer to a data buffer that contains the value to be set as a provider parameter. The form of this data varies depending on the <i>dwParam</i> value. If <i>dwParam</i> contains <b>PP_USE_HARDWARE_RNG</b>, this parameter must be <b>NULL</b>.


### -param dwFlags [in]

If <i>dwParam</i> contains <b>PP_KEYSET_SEC_DESCR</b>, <i>dwFlags</i> contains the <b>SECURITY_INFORMATION</b> applicable bit flags, as defined in the Platform SDK. Key-container security is handled by using 
<a href="https://msdn.microsoft.com/27766c97-7ac5-40fc-b798-7cd07e496c0d">SetFileSecurity</a> and 
<a href="https://msdn.microsoft.com/4043b76b-76b9-4111-8a29-a808b2412be0">GetFileSecurity</a>.

These bit flags can be combined by using a bitwise-<b>OR</b> operation. For more information, see 
<a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a>.

If <i>dwParam</i> is <b>PP_USE_HARDWARE_RNG</b> or <b>PP_DELETEKEY</b>, <i>dwFlags</i> must be set to zero.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP being used. Error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The CSP context is currently being used by another <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero or the <i>pbData</i> buffer contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwParam</i> parameter specifies an unknown parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the <i>hKey</i> key was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The function failed in some unexpected way.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a>



<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Service Provider Functions</a>
 

 

