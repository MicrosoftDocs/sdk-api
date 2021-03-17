---
UID: NF:wincrypt.CryptFindLocalizedName
title: CryptFindLocalizedName function (wincrypt.h)
description: Finds the localized name for the specified name, such as the localize name of the &quot;Root&quot; system store.
helpviewer_keywords: ["CryptFindLocalizedName","CryptFindLocalizedName function [Security]","_crypto2_cryptfindlocalizedname","security.cryptfindlocalizedname","wincrypt/CryptFindLocalizedName"]
old-location: security\cryptfindlocalizedname.htm
tech.root: security
ms.assetid: 8f0006a9-0930-4b71-87ce-e72371095e4c
ms.date: 12/05/2018
ms.keywords: CryptFindLocalizedName, CryptFindLocalizedName function [Security], _crypto2_cryptfindlocalizedname, security.cryptfindlocalizedname, wincrypt/CryptFindLocalizedName
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptFindLocalizedName
 - wincrypt/CryptFindLocalizedName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptFindLocalizedName
---

# CryptFindLocalizedName function


## -description

The <b>CryptFindLocalizedName</b> function finds the localized name for the specified name, such as the localize name of the "Root" system store. This function can be used before displaying any UI that included a name that might have a localized form.

## -parameters

### -param pwszCryptName [in]

A pointer to a specified name. An internal table is searched to compare a predefined localized name to the specified name. The search matches the localized name by using a case insensitive string comparison. 




<div class="alert"><b>Note</b>  Localized names for the predefined system stores ("Root", "My") and predefined physical stores (".Default", ".LocalMachine") are preinstalled as resource strings in Crypt32.dll.</div>
<div> </div>

## -returns

If the specified name is found, a pointer to the localized name is returned. The returned pointer must not be freed.
						

If the specified name is not found, <b>NULL</b> is returned.

## -remarks

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetoidfunctionvalue">CryptSetOIDFunctionValue</a> can be called as follows to register additional localized strings.

<i>dwEncodingType</i> = CRYPT_LOCALIZED_NAME_ENCODING_TYPE

<i>pszFuncName</i> = CRYPT_OID_FIND_LOCALIZED_NAME_FUNC

<i>pszOID</i> = CRYPT_LOCALIZED_NAME_OID

<i>pwszValueName</i> = Name to be localized, for example, L"ApplicationStore"

<i>dwValueType</i> = REG_SZ

<i>pbValueData</i> = pointer to the Unicode localized string

<i>cbValueData</i> = (wcslen(Unicode localized string) + 1) * sizeof(WCHAR)


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetoidfunctionvalue">CryptSetOIDFunctionValue</a> can be called as follows to unregister the localized strings.

<i>pbValueData</i> = <b>NULL</b>

<i>cbValueData</i> = 0.

The registered names are searched before the preinstalled names.

<table>
<tr>
<td>CRYPT_LOCALIZED_NAME_
ENCODING_TYPE

</td>
<td>0</td>
</tr>
<tr>
<td>CRYPT_LOCALIZED_NAME_
OID

</td>
<td>"LocalizedNames"</td>
</tr>
<tr>
<td>CRYPT_OID_FIND_LOCALIZED_
NAME_FUNC

</td>
<td>"CryptDLLFindLocalizedName"</td>
</tr>
</table>
 


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-setting-and-getting-certificate-store-properties">Example C Program: Setting and Getting Certificate Store Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetoidfunctionvalue">CryptSetOIDFunctionValue</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>