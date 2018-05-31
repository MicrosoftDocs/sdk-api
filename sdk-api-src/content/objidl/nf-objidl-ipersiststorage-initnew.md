---
UID: NF:objidl.IPersistStorage.InitNew
title: IPersistStorage::InitNew
author: windows-sdk-content
description: Initializes a new storage object.
old-location: com\ipersiststorage_initnew.htm
old-project: com
ms.assetid: 79caf1f6-d974-4aee-8563-eda4876a0a90
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IPersistStorage interface [COM],InitNew method, IPersistStorage.InitNew, IPersistStorage::InitNew, InitNew, InitNew method [COM], InitNew method [COM],IPersistStorage interface, _com_ipersiststorage_initnew, com.ipersiststorage_initnew, objidl/IPersistStorage::InitNew
ms.prod: windows
ms.technology: windows-sdk
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
-	IPersistStorage.InitNew
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPersistStorage::InitNew


## -description


Initializes a new storage object.


## -parameters




### -param pStg [in]

An <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the new storage object to be initialized. The container creates a nested storage object in its storage object (see <a href="https://msdn.microsoft.com/8c74cacf-8d3c-4d57-b1e9-dc5e4f281717">IStorage::CreateStorage</a>). Then, the container calls the <a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a> function to initialize the new storage object with the object class identifier (CLSID).


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
The object has already been initialized by a previous call to either the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> method or the <a href="https://msdn.microsoft.com/79caf1f6-d974-4aee-8563-eda4876a0a90">IPersistStorage::InitNew</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The storage object was not initialized due to a lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The storage object was not initialized for some reason other than a lack of memory.

</td>
</tr>
</table>
 




## -remarks



A container application can call this method when it needs to initialize a new object, for example, with an InsertObject command.

An object that supports the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface must have access to a valid storage object at all times while it is running. This includes the time just after the object has been created but before it has been made persistent. The object's container must provide the object with a valid <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage during this time through the call to <b>IPersistStorage::InitNew</b>. Depending on the container's state, a temporary file might have to be created for this purpose.

If the object wants to retain the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> instance, it must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> to increment its reference count.

After the call to <b>IPersistStorage::InitNew</b>, the object is in either the loaded or running state. For example, if the object class has an in-process server, the object will be in the running state. However, if the object uses the default handler, the container's call to <b>InitNew</b> only invokes the handler's implementation which does not run the object. Later if the container runs the object, the handler calls the <b>InitNew</b> method for the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStorage::InitNew</b> directly, you typically call the <a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a> helper function which does the following:

<ol>
<li>Calls the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function to create an instance of the object class.</li>
<li>Queries the new instance for the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface.</li>
<li>Calls the <b>InitNew</b> method to initialize the object.</li>
</ol>
The container application should cache the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> pointer to the object for use in later operations on the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An implementation of <b>IPersistStorage::InitNew</b> should initialize the object to its default state, taking the following steps:

<ol>
<li>Pre-open and cache the pointers to any streams or storages that the object will need to save itself to this storage.</li>
<li>Call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> and cache the storage pointer that is passed in.</li>
<li>Call the <a href="https://msdn.microsoft.com/ef60493c-164e-4633-a248-05c4afade937">WriteFmtUserTypeStg</a> function to write the native clipboard format and user type string for the object to the storage object.</li>
<li>Set the dirty flag for the object.</li>
</ol>
The first two steps are particularly important for ensuring that the object can save itself in low memory situations. Pre-opening and holding onto pointers to the stream and storage interfaces guarantee that a save operation to this storage will not fail due to insufficient memory.

Your implementation of this method should return the CO_E_ALREADYINITIALIZED error code if it receives a call to either the <b>IPersistStorage::InitNew</b> method or the <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a> method after it is already initialized.




## -see-also




<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>
 

 

