---
UID: NN:certenroll.IX509AttributeRenewalCertificate
title: IX509AttributeRenewalCertificate
author: windows-sdk-content
description: Represents an attribute that contains the certificate being renewed. This attribute is automatically placed in the PKCS #10 attribute collection when you call the Encode method.
old-location: security\ix509attributerenewalcertificate.htm
old-project: SecCertEnroll
ms.assetid: fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509AttributeRenewalCertificate, IX509AttributeRenewalCertificate interface [Security], IX509AttributeRenewalCertificate interface [Security],described, certenroll/IX509AttributeRenewalCertificate, security.ix509attributerenewalcertificate
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
 - IX509AttributeRenewalCertificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeRenewalCertificate interface


## -description


The <b>IX509AttributeRenewalCertificate</b> interface represents an attribute that contains the certificate being renewed. This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeRenewalCertificate</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeRenewalCertificate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeRenewalCertificate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd5a43c3-5244-43da-a6d5-87b109baea09">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the certificate to be renewed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a234755e-5b90-43f1-81f2-c2ebec9b55a4">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute by using the certificate to be renewed.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeRenewalCertificate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5c7997de-9abb-4a96-b906-a6de7378d0b1">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Retrieves the certificate to be renewed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

