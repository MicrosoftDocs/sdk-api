---
UID: NN:certenroll.ICertPropertyDescription
title: ICertPropertyDescription (certenroll.h)
author: windows-sdk-content
description: Enables you to specify and retrieve a string that contains descriptive information for a certificate.
old-location: security\icertpropertydescription.htm
tech.root: seccertenroll
ms.assetid: 229e8ce9-fe18-45f4-8f91-cd741052a134
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertPropertyDescription, ICertPropertyDescription interface [Security], ICertPropertyDescription interface [Security],described, certenroll/ICertPropertyDescription, security.icertpropertydescription
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
 - ICertPropertyDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyDescription interface


## -description


The <b>ICertPropertyDescription</b> interface enables you to specify and retrieve a string that contains descriptive information for a  certificate. You can use this interface to identify the intended purpose of a certificate for display in a user interface.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_DESCRIPTION_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyDescription</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyDescription</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyDescription</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertydescription-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains descriptive information about the certificate.

[WebEnabled] 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyDescription</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertydescription-get_description">Description</a>


</td>
<td align="left" width="63%">
Retrieves  a description of the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
 

 

