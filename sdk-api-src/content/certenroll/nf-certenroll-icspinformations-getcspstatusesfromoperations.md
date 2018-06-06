---
UID: NF:certenroll.ICspInformations.GetCspStatusesFromOperations
title: ICspInformations::GetCspStatusesFromOperations
author: windows-sdk-content
description: Retrieves an ICspStatuses collection by supported key operations and optional provider information.
old-location: security\icspinformations_getcspstatusesfromoperations_method.htm
old-project: SecCertEnroll
ms.assetid: 7c099357-8299-4664-ba16-7f8936e16054
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetCspStatusesFromOperations, GetCspStatusesFromOperations method [Security], GetCspStatusesFromOperations method [Security],ICspInformations interface, ICspInformations interface [Security],GetCspStatusesFromOperations method, ICspInformations.GetCspStatusesFromOperations, ICspInformations::GetCspStatusesFromOperations, certenroll/ICspInformations::GetCspStatusesFromOperations, security.icspinformations_getcspstatusesfromoperations_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformations.GetCspStatusesFromOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformations::GetCspStatusesFromOperations


## -description


The <b>GetCspStatusesFromOperations</b> method retrieves an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection by supported key operations and optional provider information. This method is web enabled.


## -parameters




### -param Operations [in]

An <a href="https://msdn.microsoft.com/5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289">AlgorithmOperationFlags</a> enumeration value that  specifies the supported operations. This can be a bitwise combination of the following flags:

<ul>
<li>XCN_NCRYPT_NO_OPERATION</li>
<li>XCN_NCRYPT_CIPHER_OPERATION</li>
<li>XCN_NCRYPT_HASH_OPERATION</li>
<li>XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</li>
<li>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</li>
<li>XCN_NCRYPT_SIGNATURE_OPERATION</li>
<li>XCN_NCRYPT_RNG_OPERATION</li>
<li>XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION</li>
<li>XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION</li>
<li>XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION</li>
<li>XCN_NCRYPT_EXACT_MATCH_OPERATION</li>
<li>XCN_NCRYPT_PREFERENCE_MASK_OPERATION</li>
</ul>

### -param pCspInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface that represents information for a specific provider.


### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> interface that contains the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

