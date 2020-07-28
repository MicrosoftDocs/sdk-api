---
UID: NF:certenroll.ICspAlgorithms.Add
title: ICspAlgorithms::Add (certenroll.h)
description: Adds an ICspAlgorithm object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICspAlgorithms interface","ICspAlgorithms interface [Security]","Add method","ICspAlgorithms.Add","ICspAlgorithms::Add","certenroll/ICspAlgorithms::Add","security.icspalgorithms_add_method"]
old-location: security\icspalgorithms_add_method.htm
tech.root: security
ms.assetid: 53cd408e-752c-4256-839c-e09055487c39
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICspAlgorithms interface, ICspAlgorithms interface [Security],Add method, ICspAlgorithms.Add, ICspAlgorithms::Add, certenroll/ICspAlgorithms::Add, security.icspalgorithms_add_method
f1_keywords:
- certenroll/ICspAlgorithms.Add
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
- ICspAlgorithms.Add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspAlgorithms::Add


## -description


The <b>Add</b> method adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">ICspAlgorithm</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">ICspAlgorithm</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">ICspAlgorithm</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithms">ICspAlgorithms</a>
 

 

