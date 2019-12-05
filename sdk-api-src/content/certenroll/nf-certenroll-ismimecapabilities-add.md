---
UID: NF:certenroll.ISmimeCapabilities.Add
title: ISmimeCapabilities::Add (certenroll.h)
description: Adds an ISmimeCapability object to the collection.
old-location: security\ismimecapabilities_add_method.htm
tech.root: seccertenroll
ms.assetid: 8ad35758-0dc1-4887-aea7-b8ead537cab2
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],Add method, ISmimeCapabilities.Add, ISmimeCapabilities::Add, certenroll/ISmimeCapabilities::Add, security.ismimecapabilities_add_method
ms.topic: method
f1_keywords:
- certenroll/ISmimeCapabilities.Add
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
- ISmimeCapabilities.Add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISmimeCapabilities::Add


## -description


The <b>Add</b> method adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>
 

 

