---
UID: NF:certenroll.ICertPropertyRequestOriginator.Initialize
title: ICertPropertyRequestOriginator::Initialize (certenroll.h)
description: Initializes the object from a string that contains the DNS name of the originating computer.
helpviewer_keywords: ["ICertPropertyRequestOriginator interface [Security]","Initialize method","ICertPropertyRequestOriginator.Initialize","ICertPropertyRequestOriginator::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyRequestOriginator interface","certenroll/ICertPropertyRequestOriginator::Initialize","security.icertpropertyrequestoriginator_initialize_method"]
old-location: security\icertpropertyrequestoriginator_initialize_method.htm
tech.root: security
ms.assetid: 3308dde9-ab97-40a1-9251-c207a3a66061
ms.date: 12/05/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],Initialize method, ICertPropertyRequestOriginator.Initialize, ICertPropertyRequestOriginator::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::Initialize, security.icertpropertyrequestoriginator_initialize_method
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
 - ICertPropertyRequestOriginator::Initialize
 - certenroll/ICertPropertyRequestOriginator::Initialize
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
 - ICertPropertyRequestOriginator.Initialize
---

# ICertPropertyRequestOriginator::Initialize


## -description

The <b>Initialize</b> method initializes the object from a string that contains the DNS name of the originating computer.

## -parameters

### -param strRequestOriginator [in]

A <b>BSTR</b> variable that contains the name.

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

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-get_requestoriginator">RequestOriginator</a> property to retrieve the DNS name of the originating computer.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>