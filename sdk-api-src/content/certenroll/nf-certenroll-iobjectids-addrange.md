---
UID: NF:certenroll.IObjectIds.AddRange
title: IObjectIds::AddRange (certenroll.h)
description: Adds a range of IObjectId objects to the collection.
helpviewer_keywords: ["AddRange","AddRange method [Security]","AddRange method [Security]","IObjectIds interface","IObjectIds interface [Security]","AddRange method","IObjectIds.AddRange","IObjectIds::AddRange","certenroll/IObjectIds::AddRange","security.iobjectids_addrange_method"]
old-location: security\iobjectids_addrange_method.htm
tech.root: security
ms.assetid: bf7a85a3-201b-413e-a1da-1e54b55771cc
ms.date: 12/05/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],IObjectIds interface, IObjectIds interface [Security],AddRange method, IObjectIds.AddRange, IObjectIds::AddRange, certenroll/IObjectIds::AddRange, security.iobjectids_addrange_method
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
 - IObjectIds::AddRange
 - certenroll/IObjectIds::AddRange
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
 - IObjectIds.AddRange
---

# IObjectIds::AddRange


## -description

The <b>AddRange</b> method adds a range of <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> objects to the collection.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> interface that represents the collection to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>