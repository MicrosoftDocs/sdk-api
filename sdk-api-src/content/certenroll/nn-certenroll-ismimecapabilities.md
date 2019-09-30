---
UID: NN:certenroll.ISmimeCapabilities
title: ISmimeCapabilities (certenroll.h)
author: windows-sdk-content
description: Defines the following methods and properties to manage a collection of ISmimeCapability objects.
old-location: security\ismimecapabilities.htm
tech.root: seccertenroll
ms.assetid: f9750b68-9d35-4594-96fc-2fbd54a87dcc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISmimeCapabilities, ISmimeCapabilities interface [Security], ISmimeCapabilities interface [Security],described, certenroll/ISmimeCapabilities, security.ismimecapabilities
ms.topic: interface
f1_keywords: 
 - "certenroll/ISmimeCapabilities"
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
 - ISmimeCapabilities
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISmimeCapabilities interface


## -description


The <b>ISmimeCapabilities</b> interface defines the following methods and properties to manage a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapabilities</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISmimeCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISmimeCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-add">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-addavailablesmimecapabilities">AddAvailableSmimeCapabilities</a>
</td>
<td align="left" width="63%">
Adds objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-addfromcsp">AddFromCsp</a>
</td>
<td align="left" width="63%">
Adds objects to the collection by identifying the encryption algorithms supported by a specific provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection by index value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISmimeCapabilities</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ismimecapabilities-get_itembyindex">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

