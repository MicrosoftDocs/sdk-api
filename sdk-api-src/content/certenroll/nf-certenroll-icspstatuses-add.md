---
UID: NF:certenroll.ICspStatuses.Add
title: ICspStatuses::Add (certenroll.h)
description: Adds an ICspStatus object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICspStatuses interface","ICspStatuses interface [Security]","Add method","ICspStatuses.Add","ICspStatuses::Add","certenroll/ICspStatuses::Add","security.icspstatuses_add_method"]
old-location: security\icspstatuses_add_method.htm
tech.root: security
ms.assetid: f8238071-f2e4-4533-b9bc-a86cea8086a5
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICspStatuses interface, ICspStatuses interface [Security],Add method, ICspStatuses.Add, ICspStatuses::Add, certenroll/ICspStatuses::Add, security.icspstatuses_add_method
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
 - ICspStatuses::Add
 - certenroll/ICspStatuses::Add
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
 - ICspStatuses.Add
---

# ICspStatuses::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object to the collection. This method is web enabled.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>