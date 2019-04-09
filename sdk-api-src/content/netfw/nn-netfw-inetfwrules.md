---
UID: NN:netfw.INetFwRules
title: INetFwRules (netfw.h)
author: windows-sdk-content
description: Collection of firewall rules.
old-location: ics\inetfwrules.htm
tech.root: ics
ms.assetid: 4908a5f2-4093-4f2d-8e68-fe4b2e552b13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwRules, INetFwRules interface [ICS/ICF], INetFwRules interface [ICS/ICF],described, ics.inetfwrules, netfw/INetFwRules
ms.topic: interface
req.header: netfw.h
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRules interface


## -description


The <b>INetFwRules</b> interface provides a collection of firewall rules.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRules</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwRules</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwRules</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c81bdf56-df71-425a-93d2-1fbae5ab536e">Add</a>
</td>
<td align="left" width="63%">
Adds a new rule to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3d91864-c494-449e-ae6e-819e77ddfaaa">get__NewEnum</a>
</td>
<td align="left" width="63%">
Returns an object that can be used to enumerate the rules in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a5b1103-3280-4a0c-93a7-e5d805d5bf5e">get_Count</a>
</td>
<td align="left" width="63%">
Returns the number of rules in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91c5a93b-7408-4870-a2c0-167648d849cd">Item</a>
</td>
<td align="left" width="63%">
Retrieves a rule from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70bd45c7-b5ab-43b3-afd4-2abb2a80ff0f">Remove</a>
</td>
<td align="left" width="63%">
Removes a specified rule from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRules</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c3d91864-c494-449e-ae6e-819e77ddfaaa">_NewEnum</a>


</td>
<td align="left" width="63%">
Gives access to a new enumerator for the rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0a5b1103-3280-4a0c-93a7-e5d805d5bf5e">Count</a>


</td>
<td align="left" width="63%">
Access to the number of rules in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

