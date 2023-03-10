---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET (wincrypt.h)
description: Retrieves an object.
helpviewer_keywords: ["CRYPT_OBJECT_LOCATOR_FIRST_RESERVED_USER_NAME_TYPE","CRYPT_OBJECT_LOCATOR_LAST_RESERVED_NAME_TYPE","CRYPT_OBJECT_LOCATOR_LAST_RESERVED_USER_NAME_TYPE","CRYPT_OBJECT_LOCATOR_SPN_NAME_TYPE","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET callback function [Security]","security.pfn_crypt_object_locator_provider_get","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET"]
old-location: security\pfn_crypt_object_locator_provider_get.htm
tech.root: security
ms.assetid: 2073915D-F23B-41BD-8376-4493FE9D62C6
ms.date: 12/05/2018
ms.keywords: CRYPT_OBJECT_LOCATOR_FIRST_RESERVED_USER_NAME_TYPE, CRYPT_OBJECT_LOCATOR_LAST_RESERVED_NAME_TYPE, CRYPT_OBJECT_LOCATOR_LAST_RESERVED_USER_NAME_TYPE, CRYPT_OBJECT_LOCATOR_SPN_NAME_TYPE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET callback function [Security], security.pfn_crypt_object_locator_provider_get, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET callback function


## -description

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</b> callback function retrieves an object. You must implement this function as part of your custom provider. This function is currently called by only the Secure Channel (Schannel) security package.

## -parameters

### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information.

### -param pIdentifier [in, optional]

Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPTOAPI_BLOB</a> structure that contains the object identifier. This value should always be <b>NULL</b> on the first call to this function.

### -param dwNameType [in]

The name format of the <i>pNameBlob</i> parameter. Possible values are listed below. The implementation of this function must be able to process <b>CRYPT_OBJECT_LOCATOR_SPN_NAME_TYPE</b>, which is passed in by Schannel.



#### CRYPT_OBJECT_LOCATOR_SPN_NAME_TYPE (1 (0x1))



#### CRYPT_OBJECT_LOCATOR_LAST_RESERVED_NAME_TYPE (32 (0x20))



#### CRYPT_OBJECT_LOCATOR_FIRST_RESERVED_USER_NAME_TYPE (33 (0x21))



#### CRYPT_OBJECT_LOCATOR_LAST_RESERVED_USER_NAME_TYPE (0x0000FFFF)

### -param pNameBlob [in]

Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPTOAPI_BLOB</a> structure that contains the name the calling application is using to uniquely identify the object. Your provider uses this name to locate the requested object. Schannel currently submits a DNS (domain name system) host name encoded in UTF8 with IDN names converted from punycode.

### -param ppbContent [out]

Pointer to a byte array that contains the object to be returned.

### -param pcbContent [out]

The size, in bytes, of the object pointed to by the <i>ppbContent</i> parameter.

### -param ppwszPassword [out]

Null-terminated Unicode string that contains the password, if any, used to encrypt the object. If the object is a personal information exchange (PFX) file, a password will typically be used to perform encryption. This value can be <b>NULL</b> if no password is required.

### -param ppIdentifier [out]

Address that receives a pointer to an optional identifier that can be used during subsequent calls to this function and for change notifications. For more information, see Remarks. If your provider sets this value to <b>NULL</b>, Schannel internally uses the <i>pNameBlob</i> parameter value.

## -returns

If the function succeeds, return nonzero (<b>TRUE</b>).

If the function fails, return zero (<b>FALSE</b>) and specify an appropriate error in the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function. Most errors are passed through Schannel unaltered but this behavior is not guaranteed. Some errors may be mapped to other errors.

If an object cannot be returned for a given DNS name (<i>pNameBlob</i>) or identifier (<i>pIdentifier</i>), return <b>FALSE</b> and specify <b>CRYPT_E_OBJECT_LOCATOR_OBJECT_NOT_FOUND</b> in the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function.

## -remarks

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</b> callback function is currently called by only the Secure Channel (Schannel) security package. You can return an object that encapsulates one of the following:

<ul>
<li>A personal information exchange (PFX) byte array</li>
<li>A certificate store.</li>
<li>A generic BLOB. This is not currently supported by Schannel.</li>
</ul>
When this function is first called, Schannel submits a DNS host name in the <i>pNameBlob</i> argument to specify the host for which the object is intended. Your provider must process the name (match wild cards, build a file path, and so on) to determine what object to find.

Because many host names can be mapped to one object, your provider can use the <i>ppIdentifier</i> parameter to return an internally defined identifier that can be used in subsequent calls by the cryptography API (CAPI) functions to the provider. The provider can then use the identifier to assist in finding the appropriate object.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</a>
