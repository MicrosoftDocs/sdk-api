---
UID: NF:oleidl.IOleItemContainer.GetObjectStorage
title: IOleItemContainer::GetObjectStorage method
author: windows-driver-content
description: Retrieves a pointer to the storage for the specified object.
old-location: com\ioleitemcontainer_getobjectstorage.htm
old-project: com
ms.assetid: 13a094bc-bacc-40d5-9682-ecc6072966fa
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetObjectStorage method [COM], GetObjectStorage method [COM], IOleItemContainer interface, GetObjectStorage,IOleItemContainer.GetObjectStorage, IOleItemContainer, IOleItemContainer interface [COM], GetObjectStorage method, IOleItemContainer::GetObjectStorage, _com_ioleitemcontainer_getobjectstorage, com.ioleitemcontainer_getobjectstorage, oleidl/IOleItemContainer::GetObjectStorage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleItemContainer.GetObjectStorage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOleItemContainer::GetObjectStorage method


## -description


Retrieves a pointer to the storage for the specified object.


## -parameters




### -param pszItem [in]

The compound document's name for the object whose storage is requested.


### -param pbc [in]

A pointer to the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface on the bind context to be used in this binding operation. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the binding implementation should retrieve information about its environment. 


### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object, usually <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>.


### -param ppvStorage [out]

Address of a pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvStorage</i> contains the requested interface pointer to the storage for the object named by <i>pszItem</i>. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on *<i>ppvStorage</i>; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs, *<i>ppvStorage</i> is set to <b>NULL</b>.


## -returns



This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completely successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>pszItem</i> does not identify a object in this container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
The object does not have its own independent storage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not available.

</td>
</tr>
</table>
 




## -remarks



The item moniker implementation of <a href="https://msdn.microsoft.com/94c8219f-8131-45dd-b350-878ffd6161ea">IMoniker::BindToStorage</a> calls this method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If <i>pszItem</i> designates a pseudo-object, your implementation of <b>IOleItemContainer::GetObjectStorage</b> should return MK_E_NOSTORAGE, because pseudo-objects do not have their own independent storage. If <i>pszItem</i> designates an embedded object, or a portion of the document that has its own storage, your implementation should return the specified interface pointer on the appropriate storage object.




## -see-also




<a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a>
 

 

