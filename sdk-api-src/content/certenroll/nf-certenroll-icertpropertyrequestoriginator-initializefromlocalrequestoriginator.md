---
UID: NF:certenroll.ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
title: ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator (certenroll.h)
description: Initializes the object from the DNS name of the local computer.
helpviewer_keywords: ["ICertPropertyRequestOriginator interface [Security]","InitializeFromLocalRequestOriginator method","ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator","ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator","InitializeFromLocalRequestOriginator","InitializeFromLocalRequestOriginator method [Security]","InitializeFromLocalRequestOriginator method [Security]","ICertPropertyRequestOriginator interface","certenroll/ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator","security.icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method"]
old-location: security\icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method.htm
tech.root: security
ms.assetid: 466e0767-d13a-4f5d-9715-47bb7b9d4142
ms.date: 12/05/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],InitializeFromLocalRequestOriginator method, ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator, ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator, InitializeFromLocalRequestOriginator method [Security], InitializeFromLocalRequestOriginator method [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator, security.icertpropertyrequestoriginator_initializefromlocalrequestoriginator_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator
 - certenroll/ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyRequestOriginator.InitializeFromLocalRequestOriginator
---

# ICertPropertyRequestOriginator::InitializeFromLocalRequestOriginator


## -description

The <b>InitializeFromLocalRequestOriginator</b> method initializes the object from the DNS name of the local computer.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-get_requestoriginator">RequestOriginator</a> property to retrieve the DNS name of the originating computer.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>
