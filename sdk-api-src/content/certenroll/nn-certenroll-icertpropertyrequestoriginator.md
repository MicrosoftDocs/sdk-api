---
UID: NN:certenroll.ICertPropertyRequestOriginator
title: ICertPropertyRequestOriginator (certenroll.h)
description: Represents a certificate property that contains the Domain Naming System (DNS) name of the computer on which the request was created.
helpviewer_keywords: ["ICertPropertyRequestOriginator","ICertPropertyRequestOriginator interface [Security]","ICertPropertyRequestOriginator interface [Security]","described","certenroll/ICertPropertyRequestOriginator","security.icertpropertyrequestoriginator"]
old-location: security\icertpropertyrequestoriginator.htm
tech.root: seccertenroll
ms.assetid: ce33605e-c3ae-4b96-a13e-6f06e8d5ffee
ms.date: 12/05/2018
ms.keywords: ICertPropertyRequestOriginator, ICertPropertyRequestOriginator interface [Security], ICertPropertyRequestOriginator interface [Security],described, certenroll/ICertPropertyRequestOriginator, security.icertpropertyrequestoriginator
f1_keywords:
- certenroll/ICertPropertyRequestOriginator
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
- ICertPropertyRequestOriginator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyRequestOriginator interface


## -description


The <b>ICertPropertyRequestOriginator</b> interface represents a certificate property that contains the Domain Naming System (DNS) name of the computer on which the request was  created. This property exists to reduce the potential for race conditions when using auto-enrollment to renew a certificate. Auto-enrollment attempts to renew a certificate that exists on the originating computer when the potential renewal period begins. Other computers on which that certificate is also installed and for which this property is set wait to determine whether that renewal attempt is successful. If the originating computer successfully enrolls and the new certificate is roamed to the other computers in a timely manner, the other computers will not attempt to enroll.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_REQUEST_ORIGINATOR_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyRequestOriginator</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyRequestOriginator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyRequestOriginator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains the DNS name of the originating computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-initializefromlocalrequestoriginator">InitializeFromLocalRequestOriginator</a>
</td>
<td align="left" width="63%">
Initializes the object from the DNS name of the local computer.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyRequestOriginator</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrequestoriginator-get_requestoriginator">RequestOriginator</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the DNS name of the originating computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
 

 

