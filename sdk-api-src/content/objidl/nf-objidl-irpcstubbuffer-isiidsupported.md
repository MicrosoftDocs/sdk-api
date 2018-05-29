---
UID: NF:objidl.IRpcStubBuffer.IsIIDSupported
title: IRpcStubBuffer::IsIIDSupported
author: windows-sdk-content
description: Determines whether a stub is designed to handle the unmarshaling of a particular interface.
old-location: com\irpcstubbuffer_isiidsupported.htm
old-project: com
ms.assetid: 7025d343-9171-4d0f-9e93-61365075edc0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IRpcStubBuffer interface [COM],IsIIDSupported method, IRpcStubBuffer.IsIIDSupported, IRpcStubBuffer::IsIIDSupported, IsIIDSupported, IsIIDSupported method [COM], IsIIDSupported method [COM],IRpcStubBuffer interface, _com_irpcstubbuffer_isiidsupported, com.irpcstubbuffer_isiidsupported, objidlbase/IRpcStubBuffer::IsIIDSupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
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
-	objidlbase.h
api_name:
-	IRpcStubBuffer.IsIIDSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

