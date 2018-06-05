---
UID: NN:pla.IFolderActionCollection
title: IFolderActionCollection
author: windows-sdk-content
description: Manages a collection of FolderAction objects.To get this interface, access the IDataManager::FolderActions property.
old-location: pla\ifolderactioncollection.htm
old-project: PLA
ms.assetid: 9b0ab26f-7e91-4d7a-9fd7-73332601dd7b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IFolderActionCollection, IFolderActionCollection interface [PLA], IFolderActionCollection interface [PLA],described, base.ifolderactioncollection, pla.ifolderactioncollection, pla/IFolderActionCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IFolderActionCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFolderActionCollection interface


## -description


Manages a collection of <a href="https://msdn.microsoft.com/a3942d5f-9ec4-4461-84f9-f2fae3971e23">FolderAction</a> objects.

To get this interface, access the <a href="https://msdn.microsoft.com/59fad3d2-9971-4608-8576-977d4dd8ace4">IDataManager::FolderActions</a> property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderActionCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFolderActionCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a folder action to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3ecc5e6-a6d7-4c68-b8c2-8ff94c810545">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more folder actions to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all folder actions from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caced576-cbe8-49d1-a372-70f035a6e3ed">CreateFolderAction</a>
</td>
<td align="left" width="63%">
Creates a folder action object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of folder actions in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested folder action from the collection.

</td>
</tr>
</table> 


## -remarks



You can add one or more <a href="https://msdn.microsoft.com/a3942d5f-9ec4-4461-84f9-f2fae3971e23">IFolderAction</a> instances. Each instance determines when a folder action occurs. For example, one instance  can trigger folder actions to occur at week one (<a href="https://msdn.microsoft.com/5f664ee8-895e-4235-a119-9dc10ababffe">IFolderAction::Age</a> is 7) and a second instance can trigger folder actions to occur at week 10 (<b>Age</b> is 10).



