---
UID: NN:objidl.IPersistStorage
title: IPersistStorage (objidl.h)
author: windows-sdk-content
description: Enables a container application to pass a storage object to one of its contained objects and to load and save the storage object.
old-location: com\ipersiststorage.htm
tech.root: com
ms.assetid: 1c1a20fc-c101-4cbc-a7a6-30613aa387d7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPersistStorage, IPersistStorage interface [COM], IPersistStorage interface [COM],described, _com_ipersiststorage, com.ipersiststorage, objidl/IPersistStorage
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IPersistStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistStorage interface


## -description


Enables a container application to pass a storage object to one of its contained objects and to load and save the storage object. This interface supports the structured storage model, in which each contained object has its own storage that is nested within the container's storage.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistStorage</b> interface inherits from <b>IPersist</b>. <b>IPersistStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d">HandsOffStorage</a>
</td>
<td align="left" width="63%">
Instructs the object to release all storage objects that have been passed to it by its container and to enter HandsOff mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79caf1f6-d974-4aee-8563-eda4876a0a90">InitNew</a>
</td>
<td align="left" width="63%">
Initializes a new storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/604e044f-cede-486e-8b17-c62a1cfd1d28">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">Load</a>
</td>
<td align="left" width="63%">
Loads an object from its existing storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">Save</a>
</td>
<td align="left" width="63%">
Saves an object, and any nested objects that it contains, into the specified storage object. The object enters NoScribble mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c223e7-38ce-4f20-818b-84bd4c7e0dfd">SaveCompleted</a>
</td>
<td align="left" width="63%">
Notifies the object that it can write to its storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>



<a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a>



<a href="https://msdn.microsoft.com/b8d8e1af-05a3-42f5-8672-910a2606e613">OleSave</a>
 

 

