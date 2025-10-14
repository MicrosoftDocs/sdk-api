---
UID: NF:certenroll.ICertPropertyArchived.Initialize
title: ICertPropertyArchived::Initialize (certenroll.h)
description: Initializes the object from a Boolean value that specifies whether the certificate has been archived.
helpviewer_keywords: ["ICertPropertyArchived interface [Security]","Initialize method","ICertPropertyArchived.Initialize","ICertPropertyArchived::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyArchived interface","certenroll/ICertPropertyArchived::Initialize","security.icertpropertyarchived_initialize_method"]
old-location: security\icertpropertyarchived_initialize_method.htm
tech.root: security
ms.assetid: 66efee4f-61af-447a-b668-81fbe2107b7f
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchived interface [Security],Initialize method, ICertPropertyArchived.Initialize, ICertPropertyArchived::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyArchived interface, certenroll/ICertPropertyArchived::Initialize, security.icertpropertyarchived_initialize_method
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
 - ICertPropertyArchived::Initialize
 - certenroll/ICertPropertyArchived::Initialize
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
 - ICertPropertyArchived.Initialize
---

# ICertPropertyArchived::Initialize


## -description

The <b>Initialize</b> method initializes the object from a Boolean value that specifies whether the certificate has been archived.

## -parameters

### -param ArchivedValue [in]

A <b>VARIANT_BOOL</b> variable that identifies whether the certificate has been archived.

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

 Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchived-get_archived">Archived</a> property to retrieve the Boolean value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchived">ICertPropertyArchived</a>