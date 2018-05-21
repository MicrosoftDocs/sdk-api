---
UID: NF:objidl.IBindCtx.RegisterObjectBound
title: IBindCtx::RegisterObjectBound
author: windows-driver-content
description: Registers an object with the bind context to ensure that the object remains active until the bind context is released.
old-location: com\ibindctx_registerobjectbound.htm
old-project: com
ms.assetid: 84d49231-5fdd-4a89-8e76-1f0e56bc553f
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IBindCtx interface [COM],RegisterObjectBound method, IBindCtx.RegisterObjectBound, IBindCtx::RegisterObjectBound, RegisterObjectBound, RegisterObjectBound method [COM], RegisterObjectBound method [COM],IBindCtx interface, _com_ibindctx_registerobjectbound, com.ibindctx_registerobjectbound, objidl/IBindCtx::RegisterObjectBound
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	IBindCtx.RegisterObjectBound
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBindCtx::RegisterObjectBound


## -description


Registers an object with the bind context to ensure that the object remains active until the bind context is released.


## -parameters




### -param punk [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object that is being registered as bound.


## -returns



This method can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



Those writing a new moniker class (through an implementation of the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface) should call this method whenever the implementation activates an object. This happens most often in the course of binding a moniker, but it can also happen while retrieving a moniker's display name, parsing a display name into a moniker, or retrieving the time that an object was last modified.

<b>RegisterObjectBound</b> calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> to create an additional reference to the object. You must, however, still release your own copy of the pointer. Calling this method twice for the same object creates two references to that object. You can release a reference obtained through a call to this method by calling <a href="https://msdn.microsoft.com/c49421a3-1733-4f54-8e30-d23641f13c38">IBindCtx::RevokeObjectBound</a>. All references held by the bind context are released when the bind context itself is released.

Calling <b>RegisterObjectBound</b> to register an object with a bind context keeps the object active until the bind context is released. Reusing a bind context in a subsequent binding operation (either for another piece of the same composite moniker or for a different moniker) can make the subsequent binding operation more efficient because it doesn't have to reload that object. This, however, improves performance only if the subsequent binding operation requires some of the same objects as the original one, so you need to balance the possible performance improvement of reusing a bind context against the costs of keeping objects activated unnecessarily.


<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> does not provide a method to retrieve a pointer to an object registered using <b>RegisterObjectBound</b>. Assuming the object has registered itself with the running object table, moniker implementations can call <a href="https://msdn.microsoft.com/5d74b3ee-323d-43f9-8eab-0866432659de">IRunningObjectTable::GetObject</a> to retrieve a pointer to the object.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/5d74b3ee-323d-43f9-8eab-0866432659de">IRunningObjectTable::GetObject</a>
 

 

