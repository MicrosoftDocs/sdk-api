---
UID: NF:certenroll.ICertPropertyKeyProvInfo.Initialize
title: ICertPropertyKeyProvInfo::Initialize (certenroll.h)
description: Initializes the object from a private key.
helpviewer_keywords: ["ICertPropertyKeyProvInfo interface [Security]","Initialize method","ICertPropertyKeyProvInfo.Initialize","ICertPropertyKeyProvInfo::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyKeyProvInfo interface","certenroll/ICertPropertyKeyProvInfo::Initialize","security.icertpropertykeyprovinfo_initialize_method"]
old-location: security\icertpropertykeyprovinfo_initialize_method.htm
tech.root: security
ms.assetid: bc317b7b-c4d8-480b-9de7-3324e30898b8
ms.date: 12/05/2018
ms.keywords: ICertPropertyKeyProvInfo interface [Security],Initialize method, ICertPropertyKeyProvInfo.Initialize, ICertPropertyKeyProvInfo::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyKeyProvInfo interface, certenroll/ICertPropertyKeyProvInfo::Initialize, security.icertpropertykeyprovinfo_initialize_method
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
 - ICertPropertyKeyProvInfo::Initialize
 - certenroll/ICertPropertyKeyProvInfo::Initialize
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
 - ICertPropertyKeyProvInfo.Initialize
---

# ICertPropertyKeyProvInfo::Initialize


## -description

The <b>Initialize</b> method initializes the object from a private key.

## -parameters

### -param pValue [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface that represents the private key.

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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> pointer is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ARITHMETIC_OVERFLOW</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The unique container name and the provider name are too long.

</td>
</tr>
</table>

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertykeyprovinfo-get_privatekey">PrivateKey</a> property to retrieve the key.

The <b>Initialize</b> method opens the private key and verifies that the following <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> properties are set:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspinformations">CspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_uniquecontainername">UniqueContainerName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providertype">ProviderType</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_machinecontext">MachineContext</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>