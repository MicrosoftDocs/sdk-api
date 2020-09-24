---
UID: NF:ncrypt.NCryptTranslateHandle
title: NCryptTranslateHandle function (ncrypt.h)
description: Translates a CryptoAPI handle into a CNG key handle.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","NCryptTranslateHandle","NCryptTranslateHandle function [Security]","ncrypt/NCryptTranslateHandle","security.ncrypttranslatehandle"]
old-location: security\ncrypttranslatehandle.htm
tech.root: security
ms.assetid: 0c339864-b598-430c-a597-09d3571fdbb2
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, NCryptTranslateHandle, NCryptTranslateHandle function [Security], ncrypt/NCryptTranslateHandle, security.ncrypttranslatehandle
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptTranslateHandle
 - ncrypt/NCryptTranslateHandle
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
 - NCryptTranslateHandle
---

# NCryptTranslateHandle function


## -description

The <b>NCryptTranslateHandle</b> function translates a CryptoAPI handle into a CNG key handle.

## -parameters

### -param phProvider [out, optional]

A pointer to an <b>NCRYPT_PROV_HANDLE</b> variable that receives the handle of the CNG key storage provider that owns the CNG key placed in the <i>phKey</i> parameter. This parameter can be <b>NULL</b> if this handle is not needed.

### -param phKey [out]

A pointer to a <b>NCRYPT_KEY_HANDLE</b> variable that receives the CNG key handle.

### -param hLegacyProv [in]

The handle of the CryptoAPI provider that contains the key to translate. This function will translate the CryptoAPI key that is in the container in this provider.

### -param hLegacyKey [in, optional]

The handle of a CryptoAPI key to use to help determine the key specification for the returned key. This parameter is ignored if the <i>dwLegacyKeySpec</i> parameter contains a value other than zero.

If <i>hLegacyKey</i> is <b>NULL</b> and <i>dwLegacyKeySpec</i> is zero, this function will attempt to determine the key specification from the <i>hLegacyProv</i> handle.

### -param dwLegacyKeySpec [in, optional]

Specifies the key specification for the key. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The key is none of the types below.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The key is a key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The key is a signature key.

</td>
</tr>
</table>
 

If <i>hLegacyKey</i> is <b>NULL</b> and <i>dwLegacyKeySpec</i> is zero, this function will attempt to determine the key specification from the <i>hLegacyProv</i> handle.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

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

This is a helper function intended to help applications and system components that currently use the CryptoAPI to make a graceful transition to using CNG.

This function will only be successful if a CNG key storage provider is registered with a name or alias that is identical to the name of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) referred to by the <i>hLegacyProv</i> parameter.

This function will perform the following steps to translate the CSP handle into a CNG key handle:

<ol>
<li>Obtain the name of the CSP from the <i>hLegacyProv</i> handle.</li>
<li>Open the CNG provider whose name or alias is identical to the CSP name.</li>
<li>Obtain the name of the current key container in the CSP.</li>
<li>Obtain the CryptoAPI key, translate it into a CNG key, and return it in the <i>phKey</i> parameter.</li>
</ol>
A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.