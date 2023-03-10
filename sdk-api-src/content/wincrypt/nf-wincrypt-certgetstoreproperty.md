---
UID: NF:wincrypt.CertGetStoreProperty
title: CertGetStoreProperty function (wincrypt.h)
description: Retrieves a store property.
helpviewer_keywords: ["CertGetStoreProperty","CertGetStoreProperty function [Security]","_crypto2_certgetstoreproperty","security.certgetstoreproperty","wincrypt/CertGetStoreProperty"]
old-location: security\certgetstoreproperty.htm
tech.root: security
ms.assetid: 0df4f18b-3b0f-498e-90a5-74d686af83e0
ms.date: 12/05/2018
ms.keywords: CertGetStoreProperty, CertGetStoreProperty function [Security], _crypto2_certgetstoreproperty, security.certgetstoreproperty, wincrypt/CertGetStoreProperty
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
 - CertGetStoreProperty
 - wincrypt/CertGetStoreProperty
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
 - CertGetStoreProperty
---

# CertGetStoreProperty function


## -description

The <b>CertGetStoreProperty</b> function retrieves a store property.

## -parameters

### -param hCertStore [in]

A handle of an open <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param dwPropId [in]

Indicates one of a range of store properties. There is one predefined store property, CERT_STORE_LOCALIZED_NAME_PROP_ID, the localized name of the store.

User defined properties must be outside the current range of values for predefined context properties. Currently, user defined <i>dwPropId</i> values begin at 4,096.

### -param pvData [out]

A pointer to a buffer that receives the data as determined by <i>dwPropId</i>. For CERT_STORE_LOCALIZED_NAME_PROP_ID, this is the localized name of the store, and <i>pvData</i> points to a null-terminated Unicode wide-character string. For other <i>dwPropId</i>s, <i>pvData</i> points to an array of bytes.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbData [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pvData</i> buffer. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.

If the store property is found, the function returns nonzero, <i>pvData</i> points to the property, and <i>pcbData</i> points to the length of the string. If the store property is not found, the function returns zero and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns CRYPT_E_NOT_FOUND.

## -remarks

Store property identifiers are properties applicable to an entire store. They are not properties on an individual <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), or <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context. Currently, no store properties are persisted.

To find the localized name of a store, you can also use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindlocalizedname">CryptFindLocalizedName</a> function.


#### Examples

The following example  shows querying a store for its local name property. Similar code can be used to retrieve other store properties. For a complete example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-setting-and-getting-certificate-store-properties">Example C Program: Setting and Getting Certificate Store Properties</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>


//--------------------------------------------------------------------
// Declare and initialize variables.
void *pvData = NULL;
DWORD cbData = 0;

//--------------------------------------------------------------------
// Call CertGetStoreProperty a first time
// to get the length of the store name string to be returned.
// hCertStore is a previously assigned HCERTSTORE variable that
// represents an open certificate store.
if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    NULL,     // NULL on the first call  
              // to establish the length of the string
              // to be returned
    &cbData))
{
     printf("The length of the property is %d. \n",cbData);
}
else
{
     printf("The length of the property was not calculated.\n");
     exit(1);
}

//--------------------------------------------------------------------
// cbData is the length of a string to be allocated. 
// Allocate the space for the string and call the function a 
// second time.
if(pvData = malloc(cbData))
{
     printf("%d bytes of memory allocated.\n",cbData);
}
else
{
     printf("Memory was not allocated.\n");
     exit(1);
}

// Call CertGetStoreProperty a second time
// to copy the local store name into the pvData buffer.
if(CertGetStoreProperty(
    hCertStore,
    CERT_STORE_LOCALIZED_NAME_PROP_ID,
    pvData,
    &cbData))
{
     printf("The localized name is %S.\n",pvData);
}
else
{
     printf("CertGetStoreProperty failed.\n");
     exit(1);
}

// Free memory when done.
if (pvData)
    free(pvData);

```

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetstoreproperty">CertSetStoreProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>