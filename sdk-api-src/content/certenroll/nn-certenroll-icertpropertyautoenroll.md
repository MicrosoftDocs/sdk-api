---
UID: NN:certenroll.ICertPropertyAutoEnroll
title: ICertPropertyAutoEnroll (certenroll.h)
description: Represents a certificate property that identifies a template that has been configured to enable autoenrollment of the certificate.
helpviewer_keywords: ["ICertPropertyAutoEnroll","ICertPropertyAutoEnroll interface [Security]","ICertPropertyAutoEnroll interface [Security]","described","certenroll/ICertPropertyAutoEnroll","security.icertpropertyautoenroll"]
old-location: security\icertpropertyautoenroll.htm
tech.root: security
ms.assetid: 25eab0e9-4980-49ad-9d3b-35ad47c20bcb
ms.date: 12/05/2018
ms.keywords: ICertPropertyAutoEnroll, ICertPropertyAutoEnroll interface [Security], ICertPropertyAutoEnroll interface [Security],described, certenroll/ICertPropertyAutoEnroll, security.icertpropertyautoenroll
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
 - ICertPropertyAutoEnroll
 - certenroll/ICertPropertyAutoEnroll
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
 - ICertPropertyAutoEnroll
---

# ICertPropertyAutoEnroll interface


## -description

The <b>ICertPropertyAutoEnroll</b> interface represents a certificate property that identifies a template that has been configured to enable autoenrollment of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>.

Computers and users that are joined to a domain can be automatically enrolled  for certificates to enable better management of the certificate life cycle. By default, computers are enrolled when they are restarted, and users are enrolled during logon.

The autoenrollment process copies appropriate certificate stores from Active Directory on the server to the client and enumerates the templates that have been configured for autoenrollment. A certificate request is automatically created and submitted to a certification authority for each enumerated template that requires no user interaction.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_AUTO_ENROLL_PROP_ID.</div>
<div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyAutoEnroll</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyAutoEnroll</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyAutoEnroll</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyautoenroll-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the property value by specifying the name of the template to be used for autoenrollment.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyAutoEnroll</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyautoenroll-get_templatename">TemplateName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a string that contains the name of the template that the certificate can use for autoenrollment.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>

