---
UID: NF:certenroll.IX509CertificateTemplates.Add
title: IX509CertificateTemplates::Add (certenroll.h)
description: Adds an IX509CertificateTemplate object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IX509CertificateTemplates interface","IX509CertificateTemplates interface [Security]","Add method","IX509CertificateTemplates.Add","IX509CertificateTemplates::Add","certenroll/IX509CertificateTemplates::Add","security.ix509certificatetemplates_add"]
old-location: security\ix509certificatetemplates_add.htm
tech.root: security
ms.assetid: c52186bc-af51-4369-8ff5-6122d2e80450
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509CertificateTemplates interface, IX509CertificateTemplates interface [Security],Add method, IX509CertificateTemplates.Add, IX509CertificateTemplates::Add, certenroll/IX509CertificateTemplates::Add, security.ix509certificatetemplates_add
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateTemplates::Add
 - certenroll/IX509CertificateTemplates::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509CertificateTemplates.Add
---

# IX509CertificateTemplates::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object to the collection.  This method is web enabled.

## -parameters

### -param pVal [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object to add to the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplates">IX509CertificateTemplates</a>