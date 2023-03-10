---
UID: NF:certenroll.IPolicyQualifiers.Add
title: IPolicyQualifiers::Add (certenroll.h)
description: Adds an object to the collection. (IPolicyQualifiers.Add)
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IPolicyQualifiers interface","IPolicyQualifiers interface [Security]","Add method","IPolicyQualifiers.Add","IPolicyQualifiers::Add","certenroll/IPolicyQualifiers::Add","security.ipolicyqualifiers_add_method"]
old-location: security\ipolicyqualifiers_add_method.htm
tech.root: security
ms.assetid: 41ead360-0b11-4e47-86c5-24e636cc589d
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IPolicyQualifiers interface, IPolicyQualifiers interface [Security],Add method, IPolicyQualifiers.Add, IPolicyQualifiers::Add, certenroll/IPolicyQualifiers::Add, security.ipolicyqualifiers_add_method
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
 - IPolicyQualifiers::Add
 - certenroll/IPolicyQualifiers::Add
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
 - IPolicyQualifiers.Add
---

# IPolicyQualifiers::Add


## -description

The <b>Add</b> method adds an object to the collection.

## -parameters

### -param pVal [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> interface to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a>
