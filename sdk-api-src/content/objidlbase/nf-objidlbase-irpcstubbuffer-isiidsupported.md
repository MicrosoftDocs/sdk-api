---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IRpcStubBuffer::IsIIDSupported


## -description


Determines whether a stub is designed to handle the unmarshaling of a particular interface.


## -parameters




### -param riid [in]

The IID of the interface. This parameter cannot be IID_IUnknown.


## -returns



If the stub can handle the indicated interface, then this method returns an <a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a> pointer  for that interface; otherwise, it returns <b>NULL</b>.




## -remarks



When presented with the need to remote a new IID on a given object, the RPC run time typically calls this method on all the presently-connected interface stubs in an attempt to locate one that can handle the marshaling for the request before it goes to the trouble of creating a new stub.

As in <a href="https://msdn.microsoft.com/45e2a4c3-6a78-4018-9f32-ce5523682c0f">IPSFactoryBuffer::CreateStub</a>, if a stub is presently connected to a server object, then not only must this method verify that the stub can handle the indicated interface, but it must also verify (using <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>) that the connected server object in fact supports the indicated interface. Depending on the IID and previous interface servicing requests, it may have already done so.




## -see-also




<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>
 

 

