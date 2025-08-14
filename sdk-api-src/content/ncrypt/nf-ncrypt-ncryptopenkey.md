---
UID: NF:ncrypt.NCryptOpenKey
title: NCryptOpenKey function (ncrypt.h)
description: Opens a key that exists in the specified CNG key storage provider.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","NCRYPT_MACHINE_KEY_FLAG","NCRYPT_SILENT_FLAG","NCryptOpenKey","NCryptOpenKey function [Security]","ncrypt/NCryptOpenKey","security.ncryptopenkey_func"]
old-location: security\ncryptopenkey_func.htm
tech.root: security
ms.assetid: 581c5d89-730d-4d8c-b3bb-a28edec25910
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, NCRYPT_MACHINE_KEY_FLAG, NCRYPT_SILENT_FLAG, NCryptOpenKey, NCryptOpenKey function [Security], ncrypt/NCryptOpenKey, security.ncryptopenkey_func
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
 - NCryptOpenKey
 - ncrypt/NCryptOpenKey
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
 - NCryptOpenKey
---

# NCryptOpenKey function


## -description

The <b>NCryptOpenKey</b> function opens a key that exists in the specified CNG key storage provider.

## -parameters

### -param hProvider [in]

The handle of the key storage provider to open the key from.

### -param phKey [out]

A pointer to a <b>NCRYPT_KEY_HANDLE</b> variable that receives the key handle. When you have finished using this handle, release it by passing it to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function.

### -param pszKeyName [in]

A pointer to a null-terminated Unicode string that contains the name of the key to retrieve.

### -param dwLegacyKeySpec [in]

A legacy identifier that specifies the type of key. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
The key is a key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The key is a signature key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The key is none of the above types.

</td>
</tr>
</table>

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_MACHINE_KEY_FLAG"></a><a id="ncrypt_machine_key_flag"></a><dl>
<dt><b>NCRYPT_MACHINE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Open the key for the local computer. If this flag is not present, the current user key is opened.

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
<dt><b>NTE_BAD_KEYSET</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

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

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

For performance reasons, Microsoft software-based KSPs cache private key material in the Local Security Authority (LSA) for as long as a handle to the key is open. The LSA is a privileged system process. Therefore, other users cannot access this cached copy of the key unless the user possesses administrator privileges on the system. This behavior cannot be altered through configuration.