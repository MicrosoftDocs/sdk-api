---
UID: NF:wincrypt.CertAddStoreToCollection
title: CertAddStoreToCollection function (wincrypt.h)
description: The CertAddStoreToCollection function adds a sibling certificate store to a collection certificate store.
helpviewer_keywords: ["CertAddStoreToCollection","CertAddStoreToCollection function [Security]","_crypto2_certaddstoretocollection","security.certaddstoretocollection","wincrypt/CertAddStoreToCollection"]
old-location: security\certaddstoretocollection.htm
tech.root: security
ms.assetid: ea848d74-c3ec-4166-90ea-121b33f7f318
ms.date: 12/05/2018
ms.keywords: CertAddStoreToCollection, CertAddStoreToCollection function [Security], _crypto2_certaddstoretocollection, security.certaddstoretocollection, wincrypt/CertAddStoreToCollection
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
 - CertAddStoreToCollection
 - wincrypt/CertAddStoreToCollection
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
 - CertAddStoreToCollection
---

# CertAddStoreToCollection function


## -description

The <b>CertAddStoreToCollection</b> function adds a sibling <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> to a collection certificate store. When a certificate store has been added to a collection store, all of the certificates, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs), and <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs) in the store that has been added to the collection store can be retrieved by using find or enumerate function calls that use the collection store.

## -parameters

### -param hCollectionStore [in]

Handle of a certificate store.

### -param hSiblingStore [in, optional]

Handle of a sibling store to be added to the collection store. For more information, see  Remarks.

### -param dwUpdateFlags [in]

Indicates whether <a href="/windows/desktop/SecGloss/c-gly">certificates</a>, CRLs, and CTLs can be added to the new sibling store member of the collection store. To enable addition, set <i>dwUpdateFlag</i> to CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG.   To disable additions, set <i>dwUpdateFlag</i> to zero.

### -param dwPriority [in]

Sets a priority level of the new store in the collection, with zero being the lowest priority. If zero is passed for this parameter, the specified store is appended as the last store in the collection. The priority levels of the stores in a collection determine the order in which the stores are enumerated, and the search order of the stores when attempting to retrieve a certificate, CRL, or CTL. Priority levels also determine to which store of a collection a new certificate, CRL, or CTL is added. For more information, see  Remarks.

## -returns

If the function succeeds, the function returns nonzero and a new store is added to the collection of stores.

If the function fails, it returns zero and the store was not added.

## -remarks

A collection store has the same <b>HCERTSTORE</b> handle as a single store; thus, almost all functions that apply to any <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> also apply to any collection store. Enumeration and search processes span all of the stores in a collection store; however, functions such as 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatelinktostore">CertAddCertificateLinkToStore</a> that add links to stores cannot be used with collection stores.

When a certificate, CRL, or CTL is added to a collection store, the list of sibling stores in the collection is searched in priority order to find the first store that allows adding. Adding is enabled if CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG was set in the <b>CertAddStoreToCollection</b> call. With any function that adds elements to a store, if a store that allows adding does not return success, the addition function continues on to the next store without providing notification.

When a collection store and its sibling stores are closed with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> using CERT_CLOSE_STORE_FORCE_FLAG, the collection store must be closed before its sibling stores. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the stores can be closed in any order.


#### Examples

The following example shows adding a sibling certificate store to a collection certificate store. For a full example including the complete context for this example, see 
<a href="/windows/desktop/SecCrypto/example-c-program-collection-and-sibling-certificate-store-operations">Example C Program: Collection and Sibling Certificate Store Operations</a>.


```cpp
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE  hCollectionStore = NULL;     // The collection store 
                                         // handle
HCERTSTORE  hMemoryStore = NULL;         // A memory store handle
LPCSTR pszFileName = "TestStor.sto";     // Output file name
LPWSTR pswzFirstCert = L"Full Test Cert";// Subject of the first
                                         // certificate
LPWSTR pswzSecondCert = L"Microsoft";    // Subject of the second 
                                         // certificate
//-------------------------------------------------------------------
// Open a collection certificate store.

if(hCollectionStore = CertOpenStore(
    CERT_STORE_PROV_COLLECTION, // A collection store
    0,                          // Encoding type; not used with a
                                // collection store
    NULL,                       // Use the default provider
    0,                          // No flags
    NULL))                      // Not needed

{
    printf("The collection store was opened. \n");
}
else
{
    printf( "There was an error while opening the "
        "collection store! \n");
    exit(1);
}
//-------------------------------------------------------------------
// Open a new certificate store in memory.

if(hMemoryStore = CertOpenStore(
    CERT_STORE_PROV_MEMORY,    // A memory store
    0,                         // Encoding type; not used with a
                               // memory store
    NULL,                      // Use the default provider
    0,                         // No flags
    NULL))                     // Not needed
{
    printf("The memory store was opened. \n");
}
else
{
    printf( "There was an error while opening the memory store! \n");
    exit(1);
}
//-------------------------------------------------------------------
// Add the memory store as a sibling to the collection store. 
// All certificates in the memory store and any new certificate
// added to the memory store will also be available in the 
// collection
// store.

if(CertAddStoreToCollection(
    hCollectionStore,
    hMemoryStore,
    CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG,  // New certificates can be
                                          // added to the sibling
                                          // store.
    1))                                   // The sibling store's 
                                          // priority.
                                          // Because this is the 
                                          // store with the highest
                                          // priority, certificates
                                          // added to the collection
                                          // store will actually be
                                          // stored in this store.
{
    printf("The memory store was added to the collection store.\n");
}
else
{
    printf("The memory store was not added to the "
        "collection store.\n");
    exit(1);
}


//-------------------------------------------------------------------
// The store handles must be closed.

if(CertCloseStore(hCollectionStore,
                  0))
{
    printf("The collection store was closed. \n");
}
else
{
    printf("There was an error while closing the "
        "collection store! \n");
}

if(CertCloseStore(hMemoryStore, 0))
{
    printf("The memory store was closed. \n");
}
else
{
    printf("There was an error while closing the memory store! \n");
}

```

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certremovestorefromcollection">CertRemoveStoreFromCollection</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>