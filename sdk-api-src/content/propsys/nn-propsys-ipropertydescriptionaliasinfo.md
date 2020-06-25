---
UID: NN:propsys.IPropertyDescriptionAliasInfo
title: IPropertyDescriptionAliasInfo (propsys.h)
description: Exposes methods to get the &#0034;sort by&#0034; columns properties for an item. This interface is used by UI objects that want to retrieve the primary or secondary sort columns for a given property.
helpviewer_keywords: ["IPropertyDescriptionAliasInfo","IPropertyDescriptionAliasInfo interface [Windows Properties]","IPropertyDescriptionAliasInfo interface [Windows Properties]","described","_shell_IPropertyDescriptionAliasInfo","properties.IPropertyDescriptionAliasInfo","propsys/IPropertyDescriptionAliasInfo","shell.IPropertyDescriptionAliasInfo"]
old-location: properties\IPropertyDescriptionAliasInfo.htm
tech.root: properties
ms.assetid: fc9bc0d2-3c9b-4fbc-b098-462d7d253286
ms.date: 12/05/2018
ms.keywords: IPropertyDescriptionAliasInfo, IPropertyDescriptionAliasInfo interface [Windows Properties], IPropertyDescriptionAliasInfo interface [Windows Properties],described, _shell_IPropertyDescriptionAliasInfo, properties.IPropertyDescriptionAliasInfo, propsys/IPropertyDescriptionAliasInfo, shell.IPropertyDescriptionAliasInfo
f1_keywords:
- propsys/IPropertyDescriptionAliasInfo
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyDescriptionAliasInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyDescriptionAliasInfo interface


## -description


Exposes methods to get the "sort by" columns properties for an item. This interface is used by UI objects that want to retrieve the primary or secondary sort columns for a given property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionAliasInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>. <b>IPropertyDescriptionAliasInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionaliasinfo-getadditionalsortbyaliases">GetAdditionalSortByAliases</a>
</td>
<td align="left" width="63%">
Gets the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface, which contains additional sort column values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertydescriptionaliasinfo-getsortbyalias">GetSortByAlias</a>
</td>
<td align="left" width="63%">
Gets the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface containing the primary sort column.

</td>
</tr>
</table> 

