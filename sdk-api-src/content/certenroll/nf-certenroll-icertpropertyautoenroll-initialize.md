---
UID: NF:certenroll.ICertPropertyAutoEnroll.Initialize
title: ICertPropertyAutoEnroll::Initialize (certenroll.h)
description: Initializes the object by specifying the name of the template to be used for autoenrollment.
helpviewer_keywords: ["ICertPropertyAutoEnroll interface [Security]","Initialize method","ICertPropertyAutoEnroll.Initialize","ICertPropertyAutoEnroll::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyAutoEnroll interface","certenroll/ICertPropertyAutoEnroll::Initialize","security.icertpropertyautoenroll_initialize_method"]
old-location: security\icertpropertyautoenroll_initialize_method.htm
tech.root: security
ms.assetid: f9a949c8-acd9-45b2-882e-84daf0acfad4
ms.date: 12/05/2018
ms.keywords: ICertPropertyAutoEnroll interface [Security],Initialize method, ICertPropertyAutoEnroll.Initialize, ICertPropertyAutoEnroll::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyAutoEnroll interface, certenroll/ICertPropertyAutoEnroll::Initialize, security.icertpropertyautoenroll_initialize_method
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
 - ICertPropertyAutoEnroll::Initialize
 - certenroll/ICertPropertyAutoEnroll::Initialize
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
 - ICertPropertyAutoEnroll.Initialize
---

# ICertPropertyAutoEnroll::Initialize


## -description

The <b>Initialize</b> method initializes the object by specifying the name of the template to be used for autoenrollment.

## -parameters

### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the template name or object identifier.

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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

 Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyautoenroll-get_templatename">TemplateName</a> property to retrieve the template name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyautoenroll">ICertPropertyAutoEnroll</a>