---
UID: NN:pla.IFolderActionCollection
title: IFolderActionCollection (pla.h)
description: Manages a collection of FolderAction objects.To get this interface, access the IDataManager::FolderActions property.
old-location: pla\ifolderactioncollection.htm
tech.root: PLA
ms.assetid: 9b0ab26f-7e91-4d7a-9fd7-73332601dd7b
ms.date: 12/05/2018
ms.keywords: IFolderActionCollection, IFolderActionCollection interface [PLA], IFolderActionCollection interface [PLA],described, base.ifolderactioncollection, pla.ifolderactioncollection, pla/IFolderActionCollection
f1_keywords:
- pla/IFolderActionCollection
dev_langs:
- c++
req.header: pla.h
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
req.dll: Pla.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Pla.dll
api_name:
- IFolderActionCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderActionCollection interface


## -description


Manages a collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">FolderAction</a> objects.

To get this interface, access the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_folderactions">IDataManager::FolderActions</a> property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderActionCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFolderActionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFolderActionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds a folder action to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-addrange">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more folder actions to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all folder actions from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-createfolderaction">CreateFolderAction</a>
</td>
<td align="left" width="63%">
Creates a folder action object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a folder action from the collection based on the specified index.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderActionCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of folder actions in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderactioncollection-get_item">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested folder action from the collection.

</td>
</tr>
</table> 


## -remarks



You can add one or more <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">IFolderAction</a> instances. Each instance determines when a folder action occurs. For example, one instance  can trigger folder actions to occur at week one (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ifolderaction-get_age">IFolderAction::Age</a> is 7) and a second instance can trigger folder actions to occur at week 10 (<b>Age</b> is 10).



