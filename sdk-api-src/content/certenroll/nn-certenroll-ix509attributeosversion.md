---
UID: NN:certenroll.IX509AttributeOSVersion
title: IX509AttributeOSVersion (certenroll.h)
author: windows-sdk-content
description: Represents an attribute that contains version information about the client operating system on which the certificate request was generated.
old-location: security\ix509attributeosversion.htm
tech.root: seccertenroll
ms.assetid: 2ae84d47-2bda-4954-9165-902634d09da9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeOSVersion, IX509AttributeOSVersion interface [Security], IX509AttributeOSVersion interface [Security],described, certenroll/IX509AttributeOSVersion, security.ix509attributeosversion
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
 - IX509AttributeOSVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeOSVersion interface


## -description


The <b>IX509AttributeOSVersion</b> interface represents an attribute that contains version information about the client operating system on which the certificate request was generated. The information includes the major and minor versions, the build number, and the platform identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeOSVersion</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeOSVersion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeOSVersion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f13002f-bdaa-4c82-859a-da932615dd81">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the operating system version information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eee63f8-8345-4f3d-9fee-d8d67bcebb8c">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from operating system version information.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeOSVersion</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/395ec2be-fe92-4bf1-bed3-db122e22f15e">OSVersion</a>


</td>
<td align="left" width="63%">
Retrieves the client operating system version information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

