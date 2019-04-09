---
UID: NN:xpsobjectmodel.IXpsOMDictionary
title: IXpsOMDictionary (xpsobjectmodel.h)
author: windows-sdk-content
description: The dictionary is used by an XPS package to share resources.
old-location: xps\ixpsomdictionary.htm
tech.root: printdocs
ms.assetid: f887e3d3-973c-4267-a785-6bc190c13082
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMDictionary, IXpsOMDictionary interface [XPS Documents and Packaging], IXpsOMDictionary interface [XPS Documents and Packaging],described, xps.ixpsomdictionary, xpsobjectmodel/IXpsOMDictionary
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMDictionary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDictionary interface


## -description


The dictionary is used by an XPS package to share resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDictionary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMDictionary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDictionary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69df1cdc-a965-4ea8-b1af-75176caa39ee">Append</a>
</td>
<td align="left" width="63%">
Appends an <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface along with its <i>key</i> to the end of the dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0e57247-73c2-466e-beba-b4dd09fb1f3c">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/818797dd-7255-453c-85b3-cf0c44fe5d0d">GetAt</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface pointer and the key name string of the entry at a specified index in the dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6efc2fed-e372-4416-9645-50c1430f0e75">GetByKey</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface pointer of the entry that contains the specified key.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66737d94-aa63-4f01-a446-1dffc18e8b82">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of entries in the dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd3d8ff2-8674-4669-b7c5-6f97c957cc64">GetIndex</a>
</td>
<td align="left" width="63%">
Gets the index of an <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface from the dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3570ad03-2b68-4294-b236-86bd372876a2">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the interface that contains the dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a47b7130-a3c3-44d2-a987-e78b7feb52d6">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface at a specified location in the dictionary and sets the key to identify the interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd86046b-8d87-4093-bfbd-b91e5bacba49">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases the entry from a specified location in the dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834504f6-1c79-4a88-8c7b-69efd8b798c4">SetAt</a>
</td>
<td align="left" width="63%">
Replaces the entry at a specified location in the dictionary.

</td>
</tr>
</table> 


## -remarks



The interface pointers stored in a dictionary will usually point to interfaces, such as <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>                 and <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>, that are derived from the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="https://msdn.microsoft.com/1d30e11e-1306-4721-b5fc-0419715ba2c8">IXpsOMShareable::GetType</a> method.

A dictionary cannot contain duplicate interface pointers.




## -see-also




<a href="https://msdn.microsoft.com/d0a26f36-b25d-4ab6-9779-88d01d59e41c">IXpsOMObjectFactory::CreateDictionary</a>



<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

