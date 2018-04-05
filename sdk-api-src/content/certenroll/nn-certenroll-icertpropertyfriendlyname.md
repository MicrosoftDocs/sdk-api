---
UID: NN:certenroll.ICertPropertyFriendlyName
title: ICertPropertyFriendlyName
author: windows-driver-content
description: Enables you to specify and retrieve a string that contains the display name of a certificate.
old-location: security\icertpropertyfriendlyname.htm
old-project: SecCertEnroll
ms.assetid: d2bfe2f2-423e-4620-8933-bbae4f98c62a
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: ICertPropertyFriendlyName, ICertPropertyFriendlyName interface [Security], ICertPropertyFriendlyName interface [Security], described, certenroll/ICertPropertyFriendlyName, security.icertpropertyfriendlyname
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
-	ICertPropertyFriendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyFriendlyName interface


## -description


The <b>ICertPropertyFriendlyName</b> interface enables you to specify and retrieve a string that contains the display name of a certificate.

This property is initialized during the enrollment process and associated with the dummy certificate that is temporarily copied to the request store. If the CA denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the CA issues the certificate and it is installed in the certificate store, this property is associated with the new certificate in the personal store and the dummy certificate is deleted.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_FRIENDLY_NAME_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyFriendlyName</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertyFriendlyName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyFriendlyName</b> interface has these methods.
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
Initializes the object from the certificate display name.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyFriendlyName</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7204800e-e7ae-4fc0-a221-d6f3c2b2855b">FriendlyName</a>


</td>
<td align="left" width="63%">
Retrieves the display name of the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>
 

 

