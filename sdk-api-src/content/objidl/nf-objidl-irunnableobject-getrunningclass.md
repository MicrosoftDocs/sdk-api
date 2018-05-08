---
UID: NF:objidl.IRunnableObject.GetRunningClass
title: IRunnableObject::GetRunningClass
author: windows-driver-content
description: Retrieves the CLSID of a running object.
old-location: com\irunnableobject_getrunningclass.htm
old-project: com
ms.assetid: dfe80741-ceda-44cd-8506-1807bb664ad0
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetRunningClass, GetRunningClass method [COM], GetRunningClass method [COM],IRunnableObject interface, IRunnableObject interface [COM],GetRunningClass method, IRunnableObject.GetRunningClass, IRunnableObject::GetRunningClass, _com_irunnableobject_getrunningclass, com.irunnableobject_getrunningclass, objidl/IRunnableObject::GetRunningClass
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
-	IRunnableObject.GetRunningClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRunnableObject::GetRunningClass


## -description


Retrieves the CLSID of a running object.


## -parameters




### -param lpClsid [out]

A pointer to the object's class identifier.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.




## -remarks



If an embedded document was created by an application that is not available on the user's computer, the document, by a call to <a href="https://msdn.microsoft.com/d871879f-ec68-48e1-8ef6-364cf1447d0f">CoTreatAsClass</a>, may be able to display itself for editing by emulating a class that is supported on the user's machine. In this case, the CLSID returned by a call to <b>IRunnableObject::GetRunningClass</b> will be that of the class being emulated, rather than the document's native class.




## -see-also




<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>
 

 

