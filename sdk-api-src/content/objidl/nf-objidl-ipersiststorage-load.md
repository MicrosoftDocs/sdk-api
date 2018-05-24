---
UID: NF:objidl.IPersistStorage.Load
title: IPersistStorage::Load
author: windows-driver-content
description: Loads an object from its existing storage.
old-location: com\ipersiststorage_load.htm
old-project: com
ms.assetid: 34379b8d-4e00-49cd-9fd1-65f88746c61a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IPersistStorage interface [COM],Load method, IPersistStorage.Load, IPersistStorage::Load, Load, Load method [COM], Load method [COM],IPersistStorage interface, _com_ipersiststorage_load, com.ipersiststorage_load, objidl/IPersistStorage::Load
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
-	IPersistStorage.Load
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPersistStorage::Load


## -description


Loads an object from its existing storage.


## -parameters




### -param pStg [in]

An <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the existing storage from which the object is to be loaded.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ALREADYINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized by a previous call to the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> method or the <a href="https://msdn.microsoft.com/79caf1f6-d974-4aee-8563-eda4876a0a90">IPersistStorage::InitNew</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to some reason other than a lack of memory.

</td>
</tr>
</table>
 




## -remarks



This method initializes an object from an existing storage. The object is placed in the loaded state if this method is called by the container application. If called by the default handler, this method places the object in the running state.

Either the default handler or the object itself can hold onto the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer while the object is loaded or running.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStorage::Load</b> directly, you typically call the <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a> helper function which does the following:

<ol>
<li>Create an uninitialized instance of the object class.</li>
<li>Query the new instance for the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface.</li>
<li>Call <b>Load</b> to initialize the object from the existing storage.</li>
</ol>
You also call this method indirectly when you call the <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> function or the <a href="https://msdn.microsoft.com/98c63646-6617-46b6-8c3e-82d1c4d0adb6">OleCreateFromFile</a> function to insert an object into a compound file (as in a drag-and-drop or clipboard paste operation).

The container should cache the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> pointer for use in later operations on the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation should perform the following steps to load an object:

<ol>
<li>Open the object's streams in the storage object, and read the necessary data into the object's internal data structures.</li>
<li>Clear the object's dirty flag.</li>
<li>Call the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method and cache the passed in storage pointer.</li>
<li>Keep open and cache the pointers to any streams or storages that the object will need to save itself to this storage.</li>
<li>Perform any other default initialization required for the object.</li>
</ol>
Steps 3 and 4 are particularly important for ensuring that the object can save itself in low memory situations. Holding onto pointers to the storage and stream interfaces guarantees that a save operation to this storage will not fail due to insufficient memory.

Your implementation of this method should return the CO_E_ALREADYINITIALIZED error code if it receives a call to either the <a href="https://msdn.microsoft.com/79caf1f6-d974-4aee-8563-eda4876a0a90">IPersistStorage::InitNew</a> method or the <b>IPersistStorage::Load</b> method after it is already initialized.




## -see-also




<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>



<a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a>
 

 

