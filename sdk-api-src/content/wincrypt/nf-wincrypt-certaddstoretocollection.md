---
UID: NF:wincrypt.CertAddStoreToCollection
title: CertAddStoreToCollection function
author: windows-sdk-content
description: The CertAddStoreToCollection function adds a sibling certificate store to a collection certificate store.
old-location: security\certaddstoretocollection.htm
old-project: SecCrypto
ms.assetid: ea848d74-c3ec-4166-90ea-121b33f7f318
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CertAddStoreToCollection, CertAddStoreToCollection function [Security], _crypto2_certaddstoretocollection, security.certaddstoretocollection, wincrypt/CertAddStoreToCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertAddStoreToCollection
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertAddStoreToCollection function


## -description


The <b>CertAddStoreToCollection</b> function adds a sibling <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> to a collection certificate store. When a certificate store has been added to a collection store, all of the certificates, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs), and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> (CTLs) in the store that has been added to the collection store can be retrieved by using find or enumerate function calls that use the collection store.


## -parameters




### -param hCollectionStore [in]

Handle of a certificate store.


### -param hSiblingStore [in, optional]

Handle of a sibling store to be added to the collection store. For more information, see  Remarks.


### -param dwUpdateFlags

TBD


### -param dwPriority [in]

Sets a priority level of the new store in the collection, with zero being the lowest priority. If zero is passed for this parameter, the specified store is appended as the last store in the collection. The priority levels of the stores in a collection determine the order in which the stores are enumerated, and the search order of the stores when attempting to retrieve a certificate, CRL, or CTL. Priority levels also determine to which store of a collection a new certificate, CRL, or CTL is added. For more information, see  Remarks.


#### - dwUpdateFlag [in]

Indicates whether <a href="https://msdn.microsoft.com/library/windows/hardware/mt484158">certificates</a>, CRLs, and CTLs can be added to the new sibling store member of the collection store. To enable addition, set <i>dwUpdateFlag</i> to CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG.   To disable additions, set <i>dwUpdateFlag</i> to zero.


## -returns



If the function succeeds, the function returns nonzero and a new store is added to the collection of stores.

If the function fails, it returns zero and the store was not added.




## -remarks



A collection store has the same <b>HCERTSTORE</b> handle as a single store; thus, almost all functions that apply to any <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> also apply to any collection store. Enumeration and search processes span all of the stores in a collection store; however, functions such as 
<a href="https://msdn.microsoft.com/bcbf7755-d0ce-4dd5-8462-72760364fdc3">CertAddCertificateLinkToStore</a> that add links to stores cannot be used with collection stores.

When a certificate, CRL, or CTL is added to a collection store, the list of sibling stores in the collection is searched in priority order to find the first store that allows adding. Adding is enabled if CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG was set in the <b>CertAddStoreToCollection</b> call. With any function that adds elements to a store, if a store that allows adding does not return success, the addition function continues on to the next store without providing notification.

When a collection store and its sibling stores are closed with 
<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> using CERT_CLOSE_STORE_FORCE_FLAG, the collection store must be closed before its sibling stores. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the stores can be closed in any order.


#### Examples

The following example shows adding a sibling certificate store to a collection certificate store. For a full example including the complete context for this example, see 
<a href="https://msdn.microsoft.com/5349222f-ad68-477c-8712-fde16e68f600">Example C Program: Collection and Sibling Certificate Store Operations</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//-------------------------------------------------------------------
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e1564848-8b39-4ea9-9148-142ceaaaed15">CertRemoveStoreFromCollection</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

