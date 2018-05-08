---
UID: NN:propsys.IPropertyDescriptionAliasInfo
title: IPropertyDescriptionAliasInfo
author: windows-driver-content
description: Exposes methods to get the &#0034;sort by&#0034; columns properties for an item. This interface is used by UI objects that want to retrieve the primary or secondary sort columns for a given property.
old-location: properties\IPropertyDescriptionAliasInfo.htm
old-project: properties
ms.assetid: fc9bc0d2-3c9b-4fbc-b098-462d7d253286
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: IPropertyDescriptionAliasInfo, IPropertyDescriptionAliasInfo interface [Windows Properties], IPropertyDescriptionAliasInfo interface [Windows Properties],described, _shell_IPropertyDescriptionAliasInfo, properties.IPropertyDescriptionAliasInfo, propsys/IPropertyDescriptionAliasInfo, shell.IPropertyDescriptionAliasInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyDescriptionAliasInfo
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyDescriptionAliasInfo interface


## -description


Exposes methods to get the "sort by" columns properties for an item. This interface is used by UI objects that want to retrieve the primary or secondary sort columns for a given property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionAliasInfo</b> interface inherits from <a href="shell.IPropertyDescription">IPropertyDescription</a>. <b>IPropertyDescriptionAliasInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescriptionAliasInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionAliasInfo_GetAdditionalSortByAliases">GetAdditionalSortByAliases</a>
</td>
<td align="left" width="63%">
Gets the address of a pointer to the <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a> interface, which contains additional sort column values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescriptionAliasInfo_GetSortByAlias">GetSortByAlias</a>
</td>
<td align="left" width="63%">
Gets the address of a pointer to the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface containing the primary sort column.

</td>
</tr>
</table> 

