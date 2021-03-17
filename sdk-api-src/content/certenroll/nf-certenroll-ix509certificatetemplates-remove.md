---
UID: NF:certenroll.IX509CertificateTemplates.Remove
title: IX509CertificateTemplates::Remove (certenroll.h)
description: Removes an IX509CertificateTemplate object from the collection by index number.
helpviewer_keywords: ["IX509CertificateTemplates interface [Security]","Remove method","IX509CertificateTemplates.Remove","IX509CertificateTemplates::Remove","Remove","Remove method [Security]","Remove method [Security]","IX509CertificateTemplates interface","certenroll/IX509CertificateTemplates::Remove","security.ix509certificatetemplates_remove"]
old-location: security\ix509certificatetemplates_remove.htm
tech.root: security
ms.assetid: e30aaeab-4130-40ab-9b50-32a119fdb794
ms.date: 12/05/2018
ms.keywords: IX509CertificateTemplates interface [Security],Remove method, IX509CertificateTemplates.Remove, IX509CertificateTemplates::Remove, Remove, Remove method [Security], Remove method [Security],IX509CertificateTemplates interface, certenroll/IX509CertificateTemplates::Remove, security.ix509certificatetemplates_remove
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
 - IX509CertificateTemplates::Remove
 - certenroll/IX509CertificateTemplates::Remove
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
 - IX509CertificateTemplates.Remove
---

# IX509CertificateTemplates::Remove


## -description

The <b>Remove</b> method removes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object from the collection by index number.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplates">IX509CertificateTemplates</a>