---
UID: NF:objidl.IRunnableObject.SetContainedObject
title: IRunnableObject::SetContainedObject
author: windows-sdk-content
description: Notifies an object that it is embedded in an OLE container, which ensures that reference counting is done correctly for containers that support links to embedded objects.
old-location: com\irunnableobject_setcontainedobject.htm
old-project: com
ms.assetid: dbd3f632-2b81-44d1-8376-4b507316895f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IRunnableObject interface [COM],SetContainedObject method, IRunnableObject.SetContainedObject, IRunnableObject::SetContainedObject, SetContainedObject, SetContainedObject method [COM], SetContainedObject method [COM],IRunnableObject interface, _com_irunnableobject_setcontainedobject, com.irunnableobject_setcontainedobject, objidl/IRunnableObject::SetContainedObject
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunnableObject.SetContainedObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRunnableObject::SetContainedObject


## -description


Notifies an object that it is embedded in an OLE container, which ensures that reference counting is done correctly for containers that support links to embedded objects.


## -parameters




### -param fContained [in]

<b>TRUE</b> specifies that the object is contained in an OLE container. <b>FALSE</b> indicates that it is not.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



The <b>SetContainedObject</b> method enables a container to inform an object handler that it is embedded in the container, rather than acting as a link. This call changes the container's reference on the object from strong, the default for external connections, to weak. When the object is running visibly, this method is of little significance because the end user has a lock on the object. During a silent update of an embedded link source, however, the container should not be able to hold an object in the running state after the link has been broken. For this reason, the container's reference to the object must be weak.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container application must call <b>SetContainedObject</b> if it supports linking to embedded objects. It normally makes the call immediately after calling <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a> or <a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a> and never calls the method again, even before it closes. Moreover, a container almost always calls this method with <i>fContained</i> set to <b>TRUE</b>. The use of this method with <i>fContained</i> set to <b>FALSE</b> is rare.

Calling <b>SetContainedObject</b> is optional only when you know that the embedded object will not be referenced by any client other than the container. If your container application does not support linking to embedded objects; it is preferable, but not necessary, to call <b>SetContainedObject</b>.


<a href="https://msdn.microsoft.com/154aa6f0-3c02-4139-8c8e-c2112b015fe0">OleSetContainedObject</a> is a helper function that conveniently repackages the functionality offered by <b>SetContainedObject</b>. With the release of OLE 2.01, the implementation of <b>OleSetContainedObject</b> was changed to call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>, ask for <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>, and then call <b>IRunnableObject::SetContainedObject</b>. In other words, you can use the interface and the helper function interchangeably.





## -see-also




<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>



<a href="https://msdn.microsoft.com/154aa6f0-3c02-4139-8c8e-c2112b015fe0">OleSetContainedObject</a>
 

 

