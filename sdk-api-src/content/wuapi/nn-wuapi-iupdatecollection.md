---
UID: NN:wuapi.IUpdateCollection
title: IUpdateCollection
author: windows-sdk-content
description: Represents an ordered list of updates.
old-location: wua\iupdatecollection.htm
tech.root: wua_sdk
ms.assetid: e56a09e9-6a5f-4579-9a5c-987519fccaad
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUpdateCollection, IUpdateCollection interface [Windows Update Agent], IUpdateCollection interface [Windows Update Agent],described, wua.iupdatecollection, wuapi/IUpdateCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateCollection interface


## -description


Represents an ordered list of updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IUpdateCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32b25c99-d2a0-4365-a285-f66381cfc3e7">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53b30472-ae1b-4d29-a411-25f03e515996">Clear</a>
</td>
<td align="left" width="63%">
Removes all the elements from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78a024a4-7aab-4bcb-bd3f-a79ef5580e1b">Copy</a>
</td>
<td align="left" width="63%">
Creates a shallow read/write copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/165f251e-9171-4464-8608-8f365b6598b3">Insert</a>
</td>
<td align="left" width="63%">
Inserts an item into the collection at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6d32db8-c935-41f8-a8f3-0730719cac7e">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes the item at the specified index from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/78c80163-e77a-42c1-8eb9-ec8eea5ce997">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface that can be used to enumerate the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f0d8de56-c51e-4165-a6bb-ea7eec70c567">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d36af17d-b4ac-48ef-8ca4-cc44d7f9a4ee">Item</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets an <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7443f842-8de5-4309-95bf-5ea427b25b4a">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the update collection is read-only.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateCollection coclass. Use the Microsoft.Update.UpdateColl program identifier to create the object.



