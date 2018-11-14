---
UID: NN:certenroll.ICertProperties
title: ICertProperties
author: windows-sdk-content
description: Contains methods and properties that enable you to manage a collection of certificate properties.
old-location: security\icertproperties.htm
tech.root: SecCertEnroll
ms.assetid: b830c0af-0a38-419d-8a33-8e3626c4e8f1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertProperties, ICertProperties interface [Security], ICertProperties interface [Security],described, certenroll/ICertProperties, security.icertproperties
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
 - ICertProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertProperties interface


## -description


The <b>ICertProperties</b> interface contains methods and properties that enable you to manage a collection of certificate properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertProperties</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>ICertProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375232(v=VS.85).aspx">Add</a>
</td>
<td align="left" width="63%">
Adds a property to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375233(v=VS.85).aspx">Clear</a>
</td>
<td align="left" width="63%">
Removes all properties from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375235(v=VS.85).aspx">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the collection from the properties contained in a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375237(v=VS.85).aspx">Remove</a>
</td>
<td align="left" width="63%">
Removes a property from the collection by index value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperties</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa375238(v=VS.85).aspx">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa375234(v=VS.85).aspx">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of properties in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d0e92e8a-2153-440e-829f-3c9cda8c8de4">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves a property from the collection by index number.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

