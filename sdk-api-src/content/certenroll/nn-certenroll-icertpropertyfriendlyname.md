---
UID: NN:certenroll.ICertPropertyFriendlyName
title: ICertPropertyFriendlyName
author: windows-sdk-content
description: Enables you to specify and retrieve a string that contains the display name of a certificate.
old-location: security\icertpropertyfriendlyname.htm
tech.root: seccertenroll
ms.assetid: d2bfe2f2-423e-4620-8933-bbae4f98c62a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertPropertyFriendlyName, ICertPropertyFriendlyName interface [Security], ICertPropertyFriendlyName interface [Security],described, certenroll/ICertPropertyFriendlyName, security.icertpropertyfriendlyname
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
 - ICertPropertyFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyFriendlyName interface


## -description


The <b>ICertPropertyFriendlyName</b> interface enables you to specify and retrieve a string that contains the display name of a certificate.

This property is initialized during the enrollment process and associated with the dummy certificate that is temporarily copied to the request store. If the CA denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the CA issues the certificate and it is installed in the certificate store, this property is associated with the new certificate in the personal store and the dummy certificate is deleted.<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> value is XCN_CERT_FRIENDLY_NAME_PROP_ID.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyFriendlyName</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>. <b>ICertPropertyFriendlyName</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa375721(v=VS.85).aspx">Initialize</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa375719(v=VS.85).aspx">FriendlyName</a>


</td>
<td align="left" width="63%">
Retrieves the display name of the certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375646(v=VS.85).aspx">ICertPropertyDescription</a>
 

 

