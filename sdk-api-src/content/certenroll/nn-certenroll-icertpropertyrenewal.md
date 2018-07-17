---
UID: NN:certenroll.ICertPropertyRenewal
title: ICertPropertyRenewal
author: windows-sdk-content
description: Represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed.
old-location: security\icertpropertyrenewal.htm
old-project: seccertenroll
ms.assetid: c87a391a-aec9-4b42-8084-c593ecbb0bc6
ms.author: windowssdkdev
ms.date: 07/13/2018
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyRenewal interface


## -description


The <b>ICertPropertyRenewal</b> interface represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed. This property is associated with the old certificate to identify the new certificate that replaces it.  Typically, the SHA-1 hash is referred to as the thumb print of a certificate.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_RENEWAL_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyRenewal</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertyRenewal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a SHA-1 hash of the new certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87e0eabf-7a4a-4ff2-a9ce-6482f119cafd">InitializeFromCertificateHash</a>
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

<a href="https://msdn.microsoft.com/f2ea8198-01ec-4485-9f7e-9b9fa8ddba6f">Renewal</a>


</td>
<td align="left" width="63%">
Retrieves the SHA-1 hash of the new certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

