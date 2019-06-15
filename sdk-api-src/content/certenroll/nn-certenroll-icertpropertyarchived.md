---
UID: NN:certenroll.ICertPropertyArchived
title: ICertPropertyArchived (certenroll.h)
author: windows-sdk-content
description: Represents a certificate property that identifies whether a certificate has been archived.
old-location: security\icertpropertyarchived.htm
tech.root: seccertenroll
ms.assetid: 81219ad9-4717-40e5-9ecd-d3df980e23c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchived, ICertPropertyArchived interface [Security], ICertPropertyArchived interface [Security],described, certenroll/ICertPropertyArchived, security.icertpropertyarchived
ms.topic: interface
f1_keywords: ["certenroll/ICertPropertyArchived"]
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
 - ICertPropertyArchived
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyArchived interface


## -description


The <b>ICertPropertyArchived</b> interface represents a certificate property that identifies whether a certificate has been archived. Typically, a certificate is archived after being renewed, and this property is set so that archived certificates can be identified and skipped during enumeration.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ARCHIVED_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyArchived</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyArchived</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyArchived</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchived-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a Boolean value that specifies whether the certificate has been archived.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyArchived</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchived-get_archived">Archived</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the certificate has been archived.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
 

 

