---
UID: NN:wuapi.IStringCollection
title: IStringCollection
author: windows-sdk-content
description: Represents an ordered list of strings.
old-location: wua\istringcollection.htm
tech.root: wua_sdk
ms.assetid: 3aaab669-1f80-41ee-8c29-6da613ebccff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStringCollection, IStringCollection interface [Windows Update Agent], IStringCollection interface [Windows Update Agent],described, wua.istringcollection, wuapi/IStringCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IStringCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStringCollection interface


## -description


Represents an ordered list of strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IStringCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IStringCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5412e0d-a8b7-43a6-b7a5-95d662459f78">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/480b8a8a-ecf1-4f1c-b53d-98a0151c57b5">Clear</a>
</td>
<td align="left" width="63%">
Removes all the elements from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2f6d5c0-c92a-44e5-a322-f336a3ef64ce">Copy</a>
</td>
<td align="left" width="63%">
Creates a deep read/write copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a00dde-7781-4674-bbb2-10bb2eb23548">Insert</a>
</td>
<td align="left" width="63%">
Inserts an item into the collection at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0b350b0-d5b4-49c6-acca-a50719d92262">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes the item at the specified index from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b131b276-4254-4a08-8121-3a86e28d08cb">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <b>IEnumVARIANT</b> interface that can be used to enumerate the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f735ee0b-56db-44f4-b8e6-38843098fe77">Count</a>


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

<a href="https://msdn.microsoft.com/ae92e856-ed3c-4745-827b-a5bb8e2f5938">Item</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a string in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c2556836-77a2-4f83-b16c-f9b7d2f08e3e">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the collection is read-only.

</td>
</tr>
</table> 


## -remarks



This interface can be instantiated by using the StringCollection coclass. Use the Microsoft.Update.StringColl program identifier to create the object.



