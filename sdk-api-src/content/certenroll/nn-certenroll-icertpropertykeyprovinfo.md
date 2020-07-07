---
UID: NN:certenroll.ICertPropertyKeyProvInfo
title: ICertPropertyKeyProvInfo (certenroll.h)
description: Represents a certificate property that contains information about a private key.
helpviewer_keywords: ["ICertPropertyKeyProvInfo","ICertPropertyKeyProvInfo interface [Security]","ICertPropertyKeyProvInfo interface [Security]","described","certenroll/ICertPropertyKeyProvInfo","security.icertpropertykeyprovinfo"]
old-location: security\icertpropertykeyprovinfo.htm
tech.root: seccertenroll
ms.assetid: 1c35c2f0-8e79-4031-bae2-2be081f3c8dd
ms.date: 12/05/2018
ms.keywords: ICertPropertyKeyProvInfo, ICertPropertyKeyProvInfo interface [Security], ICertPropertyKeyProvInfo interface [Security],described, certenroll/ICertPropertyKeyProvInfo, security.icertpropertykeyprovinfo
f1_keywords:
- certenroll/ICertPropertyKeyProvInfo
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- ICertPropertyKeyProvInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyKeyProvInfo interface


## -description


The <b>ICertPropertyKeyProvInfo</b> interface represents a certificate property that contains information about a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a>. The key information is contained in an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object.

This property is typically initialized by the enrollment process and associated with the dummy <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a> that is temporarily copied to the request store. If the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> marks the request pending after it is submitted, autoenrollment can later use the request ID to retrieve the certificate response. If the certification authority denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the certification authority issues the certificate and it is installed in the personal store, this property is associated with the new certificate and the dummy certificate is deleted.

When a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">smart card</a> is inserted, the smart card certificate is automatically installed in the personal store and this property is associated with it.

 Use this property whenever you need to retrieve the private key to perform a cryptographic operation.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_KEY_PROV_INFO_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyKeyProvInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyKeyProvInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyKeyProvInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertykeyprovinfo-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a private key.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyKeyProvInfo</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertykeyprovinfo-get_privatekey">PrivateKey</a>


</td>
<td align="left" width="63%">
Retrieves the private key associated with the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
 

 

