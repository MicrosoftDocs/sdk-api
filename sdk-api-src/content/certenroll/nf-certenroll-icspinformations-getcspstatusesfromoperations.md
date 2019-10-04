---
UID: NF:certenroll.ICspInformations.GetCspStatusesFromOperations
title: ICspInformations::GetCspStatusesFromOperations (certenroll.h)
author: windows-sdk-content
description: Retrieves an ICspStatuses collection by supported key operations and optional provider information.
old-location: security\icspinformations_getcspstatusesfromoperations_method.htm
tech.root: seccertenroll
ms.assetid: 7c099357-8299-4664-ba16-7f8936e16054
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCspStatusesFromOperations, GetCspStatusesFromOperations method [Security], GetCspStatusesFromOperations method [Security],ICspInformations interface, ICspInformations interface [Security],GetCspStatusesFromOperations method, ICspInformations.GetCspStatusesFromOperations, ICspInformations::GetCspStatusesFromOperations, certenroll/ICspInformations::GetCspStatusesFromOperations, security.icspinformations_getcspstatusesfromoperations_method
ms.topic: method
f1_keywords: 
 - "certenroll/ICspInformations.GetCspStatusesFromOperations"
dev_langs:
 - c++
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformations.GetCspStatusesFromOperations
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspInformations::GetCspStatusesFromOperations


## -description


The <b>GetCspStatusesFromOperations</b> method retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection by supported key operations and optional provider information. This method is web enabled.


## -parameters




### -param Operations [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-algorithmoperationflags">AlgorithmOperationFlags</a> enumeration value that  specifies the supported operations. This can be a bitwise combination of the following flags:

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

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface that represents information for a specific provider.


### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> interface that contains the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
 

 

