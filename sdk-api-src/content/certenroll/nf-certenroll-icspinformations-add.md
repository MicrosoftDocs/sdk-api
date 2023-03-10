---
UID: NF:certenroll.ICspInformations.Add
title: ICspInformations::Add (certenroll.h)
description: Adds an ICspInformation object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICspInformations interface","ICspInformations interface [Security]","Add method","ICspInformations.Add","ICspInformations::Add","certenroll/ICspInformations::Add","security.icspinformations_add_method"]
old-location: security\icspinformations_add_method.htm
tech.root: security
ms.assetid: 882d6b6c-df42-4495-8d03-fa325ccd9899
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICspInformations interface, ICspInformations interface [Security],Add method, ICspInformations.Add, ICspInformations::Add, certenroll/ICspInformations::Add, security.icspinformations_add_method
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
 - ICspInformations::Add
 - certenroll/ICspInformations::Add
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
 - ICspInformations.Add
---

# ICspInformations::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object to the collection. This method is web enabled.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>