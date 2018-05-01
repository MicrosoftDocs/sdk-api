---
UID: NN:certenroll.ICertPropertyArchived
title: ICertPropertyArchived
author: windows-driver-content
description: Represents a certificate property that identifies whether a certificate has been archived.
old-location: security\icertpropertyarchived.htm
old-project: SecCertEnroll
ms.assetid: 81219ad9-4717-40e5-9ecd-d3df980e23c6
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICertPropertyArchived, ICertPropertyArchived interface [Security], ICertPropertyArchived interface [Security], described, certenroll/ICertPropertyArchived, security.icertpropertyarchived
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertPropertyArchived
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyArchived interface


## -description


The <b>ICertPropertyArchived</b> interface represents a certificate property that identifies whether a certificate has been archived. Typically, a certificate is archived after being renewed, and this property is set so that archived certificates can be identified and skipped during enumeration.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ARCHIVED_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyArchived</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertyArchived</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
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

<a href="https://msdn.microsoft.com/c4154d9e-5a37-4a6c-9fc3-5935d8c54dc4">Archived</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the certificate has been archived.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

