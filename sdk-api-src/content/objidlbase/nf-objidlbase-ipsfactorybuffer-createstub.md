---
UID: NF:objidlbase.IPSFactoryBuffer.CreateStub
title: IPSFactoryBuffer::CreateStub (objidlbase.h)
author: windows-sdk-content
description: Creates a stub for the remote use of the specified interface.
old-location: com\ipsfactorybuffer_createstub.htm
tech.root: com
ms.assetid: 45e2a4c3-6a78-4018-9f32-ce5523682c0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateStub, CreateStub method [COM], CreateStub method [COM],IPSFactoryBuffer interface, IPSFactoryBuffer interface [COM],CreateStub method, IPSFactoryBuffer.CreateStub, IPSFactoryBuffer::CreateStub, _com_ipsfactorybuffer_createstub, com.ipsfactorybuffer_createstub, objidlbase/IPSFactoryBuffer::CreateStub
ms.topic: method
f1_keywords: 
 - "objidlbase/IPSFactoryBuffer.CreateStub"
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPSFactoryBuffer::CreateStub


## -description


Creates a stub for the remote use of the specified interface.


## -parameters




### -param riid [in]

The identifier of the interface for which a stub is to be created.


### -param pUnkServer [in]

 A controlling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface; used for aggregation.


### -param ppStub [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a> interface pointer to control marshaling.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipsfactorybuffer">IPSFactoryBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/com/stub">Stub</a>
 

 

