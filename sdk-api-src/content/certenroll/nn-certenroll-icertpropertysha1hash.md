---
UID: NN:certenroll.ICertPropertySHA1Hash
title: ICertPropertySHA1Hash (certenroll.h)
description: Represents a certificate property that contains a SHA-1 hash of the certificate.
helpviewer_keywords: ["ICertPropertySHA1Hash","ICertPropertySHA1Hash interface [Security]","ICertPropertySHA1Hash interface [Security]","described","certenroll/ICertPropertySHA1Hash","security.icertpropertysha1hash"]
old-location: security\icertpropertysha1hash.htm
tech.root: security
ms.assetid: 0946827b-c933-472c-9466-aaa3495ab202
ms.date: 12/05/2018
ms.keywords: ICertPropertySHA1Hash, ICertPropertySHA1Hash interface [Security], ICertPropertySHA1Hash interface [Security],described, certenroll/ICertPropertySHA1Hash, security.icertpropertysha1hash
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
 - ICertPropertySHA1Hash
 - certenroll/ICertPropertySHA1Hash
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
 - ICertPropertySHA1Hash
---

# ICertPropertySHA1Hash interface


## -description

The <b>ICertPropertySHA1Hash</b> interface represents a certificate property that contains a SHA-1 hash of the certificate.  The hash functions as a unique identifier. Typically, it is called a thumb print.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_SHA1_HASH_PROP_ID.</div>
<div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertySHA1Hash</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertySHA1Hash</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertySHA1Hash</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertysha1hash-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from the SHA-1 hash of a certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertySHA1Hash</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertysha1hash-get_sha1hash">SHA1Hash</a>


</td>
<td align="left" width="63%">
Retrieves the SHA-1 hash of a certificate.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>

