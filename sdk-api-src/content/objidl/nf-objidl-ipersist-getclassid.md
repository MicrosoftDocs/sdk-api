---
UID: NF:objidl.IPersist.GetClassID
title: IPersist::GetClassID
author: windows-sdk-content
description: Retrieves the class identifier (CLSID) of the object.
old-location: com\ipersist_getclassid.htm
old-project: com
ms.assetid: 921a3b86-a240-454e-9411-8d653e02b90e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetClassID, GetClassID method [COM], GetClassID method [COM],IBaseFilter interface, GetClassID method [COM],IPersist interface, GetClassID method [COM],IPersistFolder interface, IBaseFilter interface [COM],GetClassID method, IBaseFilter::GetClassID, IPersist interface [COM],GetClassID method, IPersist.GetClassID, IPersist::GetClassID, IPersistFolder interface [COM],GetClassID method, IPersistFolder::GetClassID, _com_ipersist_getclassid, com.ipersist_getclassid, objidl/IBaseFilter::GetClassID, objidl/IPersist::GetClassID, objidl/IPersistFolder::GetClassID
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
tech.root: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IPersist.GetClassID
-	IPersistFolder.GetClassID
-	IBaseFilter.GetClassID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPersist::GetClassID


## -description


Retrieves the class identifier (CLSID) of the object. 


## -parameters




### -param pClassID [out]

A pointer to the location that receives the CLSID on return. The CLSID is a globally unique identifier (GUID) that uniquely represents an object class that defines the code that can manipulate the object's data.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL. 




## -remarks



The <b>GetClassID</b> method retrieves the class identifier (CLSID) for an object, used in later operations to load object-specific code into the caller's context.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container application might call this method to retrieve the original CLSID of an object that it is treating as a different class. Such a call would be necessary if a user performed an editing operation that required the object to be saved. If the container were to save it using the treat-as CLSID, the original application would no longer be able to edit the object. Typically, in this case, the container calls the <a href="https://msdn.microsoft.com/b8d8e1af-05a3-42f5-8672-910a2606e613">OleSave</a> helper function, which performs all the necessary steps. For this reason, most container applications have no need to call this method directly.

The exception would be a container that provides an object handler for certain objects. In particular, a container application should not get an object's CLSID and then use it to retrieve class specific information from the registry. Instead, the container should use <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> and <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interfaces to retrieve such class-specific information directly from the object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Typically, implementations of this method simply supply a constant CLSID for an object. If, however, the object's <b><a href="https://msdn.microsoft.com/1d7a1677-738a-4258-9afc-e77bd0dcf40f">TreatAs</a></b> registry key has been set by an application that supports emulation (and so is treating the object as one of a different class), a call to <b>GetClassID</b> must supply the CLSID specified in the <b><a href="https://msdn.microsoft.com/1d7a1677-738a-4258-9afc-e77bd0dcf40f">TreatAs</a></b> key. For more information on emulation, see <a href="https://msdn.microsoft.com/d871879f-ec68-48e1-8ef6-364cf1447d0f">CoTreatAsClass</a>.

When an object is in the running state, the default handler calls an implementation of <b>GetClassID</b> that delegates the call to the implementation in the object. When the object is not running, the default handler instead calls the <a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a> function to read the CLSID that is saved in the object's storage.

If you are writing a custom object handler for your object, you might want to simply delegate this method to the default handler implementation (see <a href="https://msdn.microsoft.com/ffe87012-b000-4ed7-b0b2-78ffdc794d3b">OleCreateDefaultHandler</a>). 


<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
This method returns CLSID_StdURLMoniker.




## -see-also




<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a>



<a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a>



<a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>
 

 

