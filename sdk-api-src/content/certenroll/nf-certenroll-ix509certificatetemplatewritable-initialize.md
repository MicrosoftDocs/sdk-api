---
UID: NF:certenroll.IX509CertificateTemplateWritable.Initialize
title: IX509CertificateTemplateWritable::Initialize (certenroll.h)
description: Initializes an IX509CertificateTemplateWritable object from a template.
helpviewer_keywords: ["IX509CertificateTemplateWritable interface [Security]","Initialize method","IX509CertificateTemplateWritable.Initialize","IX509CertificateTemplateWritable::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509CertificateTemplateWritable interface","certenroll/IX509CertificateTemplateWritable::Initialize","security.ix509certificatetemplatewritable_initialize"]
old-location: security\ix509certificatetemplatewritable_initialize.htm
tech.root: security
ms.assetid: d70cfb65-403f-4a58-8882-393029111552
ms.date: 12/05/2018
ms.keywords: IX509CertificateTemplateWritable interface [Security],Initialize method, IX509CertificateTemplateWritable.Initialize, IX509CertificateTemplateWritable::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509CertificateTemplateWritable interface, certenroll/IX509CertificateTemplateWritable::Initialize, security.ix509certificatetemplatewritable_initialize
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
 - IX509CertificateTemplateWritable::Initialize
 - certenroll/IX509CertificateTemplateWritable::Initialize
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
 - IX509CertificateTemplateWritable.Initialize
---

# IX509CertificateTemplateWritable::Initialize


## -description

The <b>Initialize</b> method initializes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> object from a template.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> interface that represents a certificate request template.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE </b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter does not point to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> has already been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a>