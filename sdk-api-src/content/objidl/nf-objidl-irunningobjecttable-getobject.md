---
UID: NF:objidl.IRunningObjectTable.GetObject
title: IRunningObjectTable::GetObject
author: windows-driver-content
description: Determines whether the object identified by the specified moniker is running, and if it is, retrieves a pointer to that object.
old-location: com\irunningobjecttable_getobject.htm
old-project: com
ms.assetid: 5d74b3ee-323d-43f9-8eab-0866432659de
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetObject, GetObject method [COM], GetObject method [COM],IRunningObjectTable interface, IRunningObjectTable interface [COM],GetObject method, IRunningObjectTable.GetObject, IRunningObjectTable::GetObject, _com_irunningobjecttable_getobject, com.irunningobjecttable_getobject, objidl/IRunningObjectTable::GetObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IRunningObjectTable.GetObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRunningObjectTable::GetObject


## -description


Determines whether the object identified by the specified moniker is running, and if it is, retrieves a pointer to that object.


## -parameters




### -param pmkObjectName [in]

A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker.


### -param ppunkObject [out]

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer variable that receives the interface pointer to the running object. When successful, the implementation calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the object; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If the object is not running or if an error occurs, the implementation sets *<i>ppunkObject</i> to <b>NULL</b>.


## -returns



This method can return the following values.

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
Indicates that <i>pmkObjectName</i> was found in the ROT and a pointer was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no entry for <i>pmkObjectName</i> in the ROT, or that the object it identifies is no longer running (in which case, the entry is revoked).

</td>
</tr>
</table>
 




## -remarks



This method checks the ROT for the moniker specified by <i>pmkObjectName</i>. If that moniker had previously been registered with a call to <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a>, this method returns the pointer that was registered at that time.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Generally, you call the <b>IRunningObjectTable::GetObject</b> method only if you are writing your own moniker class (that is, implementing the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface). You typically call this method from your implementation of <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a>.

However, note that not all implementations of <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> need to call this method. If you expect your moniker to have a prefix (indicated by a non-<b>NULL</b><i>pmkToLeft</i> parameter to <b>IMoniker::BindToObject</b>), you should not check the ROT. The reason for this is that only complete monikers are registered with the ROT, and if your moniker has a prefix, your moniker is part of a composite and thus not complete. Instead, your moniker should request services from the object identified by the prefix (for example, the container of the object identified by your moniker).




## -see-also




<a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

