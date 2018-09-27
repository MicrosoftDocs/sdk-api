---
UID: NN:certenroll.IX509AttributeRenewalCertificate
title: IX509AttributeRenewalCertificate
author: windows-sdk-content
description: Represents an attribute that contains the certificate being renewed. This attribute is automatically placed in the PKCS #10 attribute collection when you call the Encode method.
old-location: security\ix509attributerenewalcertificate.htm
tech.root: seccertenroll
ms.assetid: fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab
ms.author: windowssdkdev
ms.date: 08/31/2018
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
 - IX509AttributeRenewalCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeRenewalCertificate interface


## -description


The <b>IX509AttributeRenewalCertificate</b> interface represents an attribute that contains the certificate being renewed. This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeRenewalCertificate</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>. <b>IX509AttributeRenewalCertificate</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377103(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the certificate to be renewed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377104(v=VS.85).aspx">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377107(v=VS.85).aspx">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Retrieves the certificate to be renewed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

