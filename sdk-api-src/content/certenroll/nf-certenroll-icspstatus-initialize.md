---
UID: NF:certenroll.ICspStatus.Initialize
title: ICspStatus::Initialize (certenroll.h)
description: Initializes the object from a cryptographic provider and an associated algorithm.
helpviewer_keywords: ["ICspStatus interface [Security]","Initialize method","ICspStatus.Initialize","ICspStatus::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICspStatus interface","certenroll/ICspStatus::Initialize","security.icspstatus_initialize"]
old-location: security\icspstatus_initialize.htm
tech.root: security
ms.assetid: dc5f92e8-29fe-474c-bf1d-c6d7716abce1
ms.date: 12/05/2018
ms.keywords: ICspStatus interface [Security],Initialize method, ICspStatus.Initialize, ICspStatus::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICspStatus interface, certenroll/ICspStatus::Initialize, security.icspstatus_initialize
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
 - ICspStatus::Initialize
 - certenroll/ICspStatus::Initialize
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
 - ICspStatus.Initialize
---

# ICspStatus::Initialize


## -description

The <b>Initialize</b> method initializes the object from a cryptographic provider and an associated algorithm. This method is web enabled.

## -parameters

### -param pCsp [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface that represents information about the provider.

### -param pAlgorithm [in, optional]

Pointer to an  <a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> interface that represents an algorithm supported by the provider identified in the  <i>pCsp</i> parameter. This parameter is optional and can be <b>NULL</b>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

The <b>Initialize</b> method saves the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> and <a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> objects you specify in the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_cspinformation">CspInformation</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_cspalgorithm">CspAlgorithm</a> properties. The method also creates an empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> object and saves it in the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatus-get_enrollmentstatus">EnrollmentStatus</a> property.

An <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection is typically initialized by an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object. The <b>Initialize</b> method has been provided so that you can create <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects to add to a custom collection.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>