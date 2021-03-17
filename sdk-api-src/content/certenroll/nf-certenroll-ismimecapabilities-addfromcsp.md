---
UID: NF:certenroll.ISmimeCapabilities.AddFromCsp
title: ISmimeCapabilities::AddFromCsp (certenroll.h)
description: Adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.
helpviewer_keywords: ["AddFromCsp","AddFromCsp method [Security]","AddFromCsp method [Security]","ISmimeCapabilities interface","ISmimeCapabilities interface [Security]","AddFromCsp method","ISmimeCapabilities.AddFromCsp","ISmimeCapabilities::AddFromCsp","certenroll/ISmimeCapabilities::AddFromCsp","security.ismimecapabilities_addfromcsp_method"]
old-location: security\ismimecapabilities_addfromcsp_method.htm
tech.root: security
ms.assetid: a4244a4e-6ec3-4c1f-a0d6-607cc942b5f5
ms.date: 12/05/2018
ms.keywords: AddFromCsp, AddFromCsp method [Security], AddFromCsp method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],AddFromCsp method, ISmimeCapabilities.AddFromCsp, ISmimeCapabilities::AddFromCsp, certenroll/ISmimeCapabilities::AddFromCsp, security.ismimecapabilities_addfromcsp_method
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
 - ISmimeCapabilities::AddFromCsp
 - certenroll/ISmimeCapabilities::AddFromCsp
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
 - ISmimeCapabilities.AddFromCsp
---

# ISmimeCapabilities::AddFromCsp


## -description

The <b>AddFromCsp</b> method adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface that represents the provider.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>