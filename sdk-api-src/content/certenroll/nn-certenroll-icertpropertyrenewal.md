---
UID: NN:certenroll.ICertPropertyRenewal
title: ICertPropertyRenewal
author: windows-sdk-content
description: Represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed.
old-location: security\icertpropertyrenewal.htm
tech.root: seccertenroll
ms.assetid: c87a391a-aec9-4b42-8084-c593ecbb0bc6
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICertPropertyRenewal, ICertPropertyRenewal interface [Security], ICertPropertyRenewal interface [Security],described, certenroll/ICertPropertyRenewal, security.icertpropertyrenewal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ICertPropertyRenewal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyRenewal interface


## -description


The <b>ICertPropertyRenewal</b> interface represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed. This property is associated with the old certificate to identify the new certificate that replaces it.  Typically, the SHA-1 hash is referred to as the thumb print of a certificate.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> value is XCN_CERT_RENEWAL_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyRenewal</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>. <b>ICertPropertyRenewal</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyRenewal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375755(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a SHA-1 hash of the new certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375753(v=VS.85).aspx">InitializeFromCertificateHash</a>
</td>
<td align="left" width="63%">
Initializes the object from the new  certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyRenewal</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa375766(v=VS.85).aspx">Renewal</a>


</td>
<td align="left" width="63%">
Retrieves the SHA-1 hash of the new certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>
 

 

