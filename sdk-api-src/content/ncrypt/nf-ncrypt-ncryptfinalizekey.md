---
UID: NF:ncrypt.NCryptFinalizeKey
title: NCryptFinalizeKey function (ncrypt.h)
description: Completes a CNG key storage key.
helpviewer_keywords: ["NCRYPT_NO_KEY_VALIDATION","NCRYPT_SILENT_FLAG","NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG","NCryptFinalizeKey","NCryptFinalizeKey function [Security]","ncrypt/NCryptFinalizeKey","security.ncryptfinalizekey_func"]
old-location: security\ncryptfinalizekey_func.htm
tech.root: security
ms.assetid: 4386030d-4ce6-4b2e-adc5-a15ddc869349
ms.date: 12/05/2018
ms.keywords: NCRYPT_NO_KEY_VALIDATION, NCRYPT_SILENT_FLAG, NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG, NCryptFinalizeKey, NCryptFinalizeKey function [Security], ncrypt/NCryptFinalizeKey, security.ncryptfinalizekey_func
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
 - NCryptFinalizeKey
 - ncrypt/NCryptFinalizeKey
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
 - NCryptFinalizeKey
---

# NCryptFinalizeKey function


## -description

The <b>NCryptFinalizeKey</b> function completes a CNG key storage key. The key cannot be used until this function has been called.

## -parameters

### -param hKey [in]

The handle of the key to complete. This handle is obtained by calling the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptcreatepersistedkey">NCryptCreatePersistedKey</a> function.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_NO_KEY_VALIDATION"></a><a id="ncrypt_no_key_validation"></a><dl>
<dt><b>NCRYPT_NO_KEY_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
Do not validate the public portion of the key pair. This flag only applies to public/private key pairs.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG"></a><a id="ncrypt_write_key_to_legacy_store_flag"></a><dl>
<dt><b>NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Also save the key in legacy storage. This allows the key to be used with CryptoAPI. This flag only applies to RSA keys.

</td>
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
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.