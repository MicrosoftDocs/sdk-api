---
UID: NN:objidl.IPersistStorage
title: IPersistStorage (objidl.h)
description: Enables a container application to pass a storage object to one of its contained objects and to load and save the storage object.
helpviewer_keywords: ["IPersistStorage","IPersistStorage interface [COM]","IPersistStorage interface [COM]","described","_com_ipersiststorage","com.ipersiststorage","objidl/IPersistStorage"]
old-location: com\ipersiststorage.htm
tech.root: com
ms.assetid: 1c1a20fc-c101-4cbc-a7a6-30613aa387d7
ms.date: 12/05/2018
ms.keywords: IPersistStorage, IPersistStorage interface [COM], IPersistStorage interface [COM],described, _com_ipersiststorage, com.ipersiststorage, objidl/IPersistStorage
f1_keywords:
- objidl/IPersistStorage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-handsoffstorage">HandsOffStorage</a>
</td>
<td align="left" width="63%">
Instructs the object to release all storage objects that have been passed to it by its container and to enter HandsOff mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">InitNew</a>
</td>
<td align="left" width="63%">
Initializes a new storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">Load</a>
</td>
<td align="left" width="63%">
Loads an object from its existing storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">Save</a>
</td>
<td align="left" width="63%">
Saves an object, and any nested objects that it contains, into the specified storage object. The object enters NoScribble mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted">SaveCompleted</a>
</td>
<td align="left" width="63%">
Notifies the object that it can write to its storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a>
 

 

