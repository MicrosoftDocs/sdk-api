---
UID: NN:certenroll.IObjectIds
title: IObjectIds
author: windows-sdk-content
description: The IObjectIds interface defines methods and properties that enable you to manage a collection of IObjectId objects.
old-location: security\iobjectids.htm
old-project: SecCertEnroll
ms.assetid: f376a33e-005b-4810-9a26-b642236ff7af
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IObjectIds, IObjectIds interface [Security], IObjectIds interface [Security],described, certenroll/IObjectIds, security.iobjectids
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
 - IObjectIds
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectIds interface


## -description


The <b>IObjectIds</b> interface defines methods and properties that enable you to manage a collection of <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectIds</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IObjectIds</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IObjectIds</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf7a85a3-201b-413e-a1da-1e54b55771cc">AddRange</a>
</td>
<td align="left" width="63%">
Adds a range of <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> objects to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object from the collection by index value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectIds</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/388c3ac4-9b3b-46a5-9b8f-d446de92f6c2">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>
 

 

