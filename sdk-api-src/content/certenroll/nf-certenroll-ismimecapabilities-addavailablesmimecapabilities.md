---
UID: NF:certenroll.ISmimeCapabilities.AddAvailableSmimeCapabilities
title: ISmimeCapabilities::AddAvailableSmimeCapabilities (certenroll.h)
description: Adds ISmimeCapability objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.
helpviewer_keywords: ["AddAvailableSmimeCapabilities","AddAvailableSmimeCapabilities method [Security]","AddAvailableSmimeCapabilities method [Security]","ISmimeCapabilities interface","ISmimeCapabilities interface [Security]","AddAvailableSmimeCapabilities method","ISmimeCapabilities.AddAvailableSmimeCapabilities","ISmimeCapabilities::AddAvailableSmimeCapabilities","certenroll/ISmimeCapabilities::AddAvailableSmimeCapabilities","security.ismimecapabilities_addavailablesmimecapabilities_method"]
old-location: security\ismimecapabilities_addavailablesmimecapabilities_method.htm
tech.root: security
ms.assetid: b3b087e7-9934-4d29-a516-db5bba824774
ms.date: 12/05/2018
ms.keywords: AddAvailableSmimeCapabilities, AddAvailableSmimeCapabilities method [Security], AddAvailableSmimeCapabilities method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],AddAvailableSmimeCapabilities method, ISmimeCapabilities.AddAvailableSmimeCapabilities, ISmimeCapabilities::AddAvailableSmimeCapabilities, certenroll/ISmimeCapabilities::AddAvailableSmimeCapabilities, security.ismimecapabilities_addavailablesmimecapabilities_method
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
 - ISmimeCapabilities::AddAvailableSmimeCapabilities
 - certenroll/ISmimeCapabilities::AddAvailableSmimeCapabilities
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
 - ISmimeCapabilities.AddAvailableSmimeCapabilities
---

# ISmimeCapabilities::AddAvailableSmimeCapabilities


## -description

The <b>AddAvailableSmimeCapabilities</b> method adds <a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.

## -parameters

### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that identifies the certificate store context. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>