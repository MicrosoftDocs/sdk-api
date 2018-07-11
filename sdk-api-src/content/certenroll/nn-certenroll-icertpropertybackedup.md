---
UID: NN:certenroll.ICertPropertyBackedUp
title: ICertPropertyBackedUp
author: windows-sdk-content
description: Represents an external certificate property that identifies whether a certificate has been backed up and, if so, the date and time that it was saved.
old-location: security\icertpropertybackedup.htm
old-project: seccertenroll
ms.assetid: 9c694991-6f2d-420e-9f9f-5a36b10c39aa
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ICertPropertyBackedUp, ICertPropertyBackedUp interface [Security], ICertPropertyBackedUp interface [Security],described, certenroll/ICertPropertyBackedUp, security.icertpropertybackedup
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
 - ICertPropertyBackedUp
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyBackedUp interface


## -description


The <b>ICertPropertyBackedUp</b> interface represents an external certificate property that identifies whether a certificate has been backed up and, if so, the date and time that it was saved. This property is not currently used.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_BACKED_UP_PROP_ID.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyBackedUp</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertyBackedUp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyBackedUp</b> interface has these methods.
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
Initializes the object from a Boolean value and a date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2033c947-661c-4a52-b24f-82fa71ba7868">InitializeFromCurrentTime</a>
</td>
<td align="left" width="63%">
Initializes the property from a Boolean value and the current system date and time.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyBackedUp</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5515fbd5-a711-421d-b80d-3e77c83f7549">BackedUpTime</a>


</td>
<td align="left" width="63%">
Retrieves the date and time at which the certificate was backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/206ef65a-93c5-4c0d-b673-42a0b065225c">BackedUpValue</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that identifies whether the certificate was backed up.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

