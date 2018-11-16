---
UID: NN:azroles.IAzApplicationGroups
title: IAzApplicationGroups
author: windows-sdk-content
description: Represents a collection of IAzApplicationGroup objects.
old-location: security\iazapplicationgroups.htm
tech.root: SecAuthZ
ms.assetid: e96c4cae-0a0a-4ac4-805f-2042312f0267
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAzApplicationGroups, IAzApplicationGroups interface [Security], IAzApplicationGroups interface [Security],described, azroles/IAzApplicationGroups, security.iazapplicationgroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplicationGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroups interface


## -description


The <b>IAzApplicationGroups</b> interface represents a collection of  
<a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroups</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzApplicationGroups</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzApplicationGroups</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/412fe347-63cb-4f87-98e1-2d8665f39a6a">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/412fe347-63cb-4f87-98e1-2d8665f39a6a">_NewEnum</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d57e4428-3666-4eb0-8157-8b35acfc517b">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d57e4428-3666-4eb0-8157-8b35acfc517b">Count</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b895379-9b2f-45f5-997e-b589f08d7d6e">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/9b895379-9b2f-45f5-997e-b589f08d7d6e">Item</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplicationGroups</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/412fe347-63cb-4f87-98e1-2d8665f39a6a">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface on an object that can be used to enumerate the collection. This property is hidden within Visual Basic and Visual Basic Scripting Edition (VBScript).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d57e4428-3666-4eb0-8157-8b35acfc517b">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9b895379-9b2f-45f5-997e-b589f08d7d6e">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object at the specified index into the <b>IAzApplicationGroups</b> collection.

</td>
</tr>
</table> 

