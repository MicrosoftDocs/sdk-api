---
UID: NF:objidl.IPSFactoryBuffer.CreateStub
title: IPSFactoryBuffer::CreateStub
author: windows-sdk-content
description: Creates a stub for the remote use of the specified interface.
old-location: com\ipsfactorybuffer_createstub.htm
old-project: com
ms.assetid: 45e2a4c3-6a78-4018-9f32-ce5523682c0f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CreateStub, CreateStub method [COM], CreateStub method [COM],IPSFactoryBuffer interface, IPSFactoryBuffer interface [COM],CreateStub method, IPSFactoryBuffer.CreateStub, IPSFactoryBuffer::CreateStub, _com_ipsfactorybuffer_createstub, com.ipsfactorybuffer_createstub, objidlbase/IPSFactoryBuffer::CreateStub
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPSFactoryBuffer.CreateStub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPSFactoryBuffer::CreateStub


## -description


Creates a stub for the remote use of the specified interface.


## -parameters




### -param riid [in]

The identifier of the interface for which a stub is to be created.


### -param pUnkServer [in]

 A controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface; used for aggregation.


### -param ppStub [out]

A pointer to an <a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a> interface pointer to control marshaling.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ffe85701-a4fa-4cf3-9b86-85f3a0cb63e9">IPSFactoryBuffer</a>



<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>



<a href="https://msdn.microsoft.com/ed7d5546-2d19-4055-b078-62b39d0317b7">Stub</a>
 

 

