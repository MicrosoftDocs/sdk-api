---
UID: NN:azroles.IAzRoles
title: IAzRoles (azroles.h)

description: Represents a collection of IAzRole objects.
old-location: security\iazroles.htm
tech.root: SecAuthZ
ms.assetid: bc69ec52-ea73-4a0c-a9a2-913a6725489e

ms.date: 12/05/2018
ms.keywords: IAzRoles, IAzRoles interface [Security], IAzRoles interface [Security],described, azroles/IAzRoles, security.iazroles
ms.topic: interface
f1_keywords: 
 - "azroles/IAzRoles"
dev_langs:
 - c++
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
 - IAzRoles
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzRoles interface


## -description


The <b>IAzRoles</b> interface represents a collection of  
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoles</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzRoles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzRoles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get__newenum">_NewEnum</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_count">Count</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_item">Item</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzRoles</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface on an object that can be used to enumerate the collection. This property is hidden within Visual Basic and Visual Basic Scripting Edition (VBScript).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazroles-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object at the specified index into the <b>IAzRoles</b> collection.

</td>
</tr>
</table> 

