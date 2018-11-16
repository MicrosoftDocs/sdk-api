---
UID: NN:functiondiscoveryapi.IFunctionInstanceCollection
title: IFunctionInstanceCollection
author: windows-sdk-content
description: Represents a group of IFunctionInstance objects returned as the result of a query or get instance request.
old-location: ncd\ifunctioninstancecollection.htm
tech.root: FunDisc
ms.assetid: 8ac1a406-92f3-4e39-985e-ab8fa7d28751
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFunctionInstanceCollection, IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,described, functiondiscoveryapi/IFunctionInstanceCollection, ncd.ifunctioninstancecollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceCollection interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface represents a group of <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> objects returned as the result of a query or get instance request through one of the <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a> methods; client program do not create these collections themselves.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionInstanceCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstanceCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c77729f2-2524-4502-82d6-3a3be8344d94">Add</a>
</td>
<td align="left" width="63%">
Adds a function instance to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7f94912-9656-4a6b-8754-eb37358b5f9d">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified function instance from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d56a16a-d44a-4c7c-931d-b5f6708cb7d6">DeleteAll</a>
</td>
<td align="left" width="63%">
Removes all function instances from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3db880-a765-4a18-91ac-d091728cbb39">Get</a>
</td>
<td align="left" width="63%">
Gets the specified function instance and its index from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d74d10b1-dab1-4f7e-8dbc-434570bf9c79">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of function instances in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b79b7cb2-c02a-4474-bd48-8907ebb118fa">Item</a>
</td>
<td align="left" width="63%">
Gets the specified function instance, by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5abe3e0-a07c-45e4-a590-133f6b30a7f7">Remove</a>
</td>
<td align="left" width="63%">
Deletes the specified function instance and returns a pointer to the function instance being removed.

</td>
</tr>
</table> 


## -remarks



The <b>IFunctionInstanceCollection</b> interface allows a client program to enumerate a collection of  <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> objects.



