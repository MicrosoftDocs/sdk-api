---
UID: NF:unknwn.IUnknown.QueryInterface(Q,)
title: IUnknown::QueryInterface(Q,)
author: windows-sdk-content
description: Retrieves pointers to the supported interfaces on an object.
old-location: com\iunknown_queryinterface.htm
old-project: com
ms.assetid: 54d5ff80-18db-43f2-b636-f93ac053146d
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IUnknown interface [COM],QueryInterface method, IUnknown.QueryInterface, IUnknown.QueryInterface(Q,), IUnknown::QueryInterface, IUnknown::QueryInterface(Q,), QueryInterface, QueryInterface method [COM], QueryInterface method [COM],IUnknown interface, _com_iunknown_queryinterface, com.iunknown_queryinterface, unknwn/IUnknown::QueryInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: unknwn.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unknwn.h
api_name:
 - IUnknown.QueryInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IUnknown::QueryInterface(Q,)


## -description


Retrieves pointers to the supported interfaces on an object.

This method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the pointer it returns.


## -parameters




### -param pp




### -param param






#### - ppvObject [out]

The address of a pointer variable that receives the interface pointer requested in the <i>riid</i> parameter. Upon successful return, *<i>ppvObject</i> contains the requested interface pointer to the object. If the object does not support the interface, *<i>ppvObject</i> is set to <b>NULL</b>.


#### - riid [in]

The identifier of the interface being requested.


## -returns



This method returns S_OK if the interface is supported, and E_NOINTERFACE otherwise. If <i>ppvObject</i> is <b>NULL</b>, this method returns E_POINTER.




## -remarks



For any one object, a specific query for the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on any of the object's interfaces must always return the same pointer value. This enables a client to determine whether two pointers point to the same component by calling <b>QueryInterface</b> with IID_IUnknown and comparing the results. It is specifically not the case that queries for interfaces other than IUnknown (even the same interface through the same pointer) must return the same pointer value.

There are four requirements for implementations of <b>QueryInterface</b> (In these cases, "must succeed" means "must succeed barring catastrophic failure."):

<ul>
<li>
The set of interfaces accessible on an object through <b>QueryInterface</b> must be static, not dynamic. This means that if a call to <b>QueryInterface</b> for a pointer to a specified interface succeeds the first time, it must succeed again, and if it fails the first time, it must fail on all subsequent queries.

</li>
<li>
It must be reflexive â€” if a client holds a pointer to an interface on an object, and queries for that interface, the call must succeed.

</li>
<li>
It must be symmetric â€” if a client holding a pointer to one interface queries successfully for another, a query through the obtained pointer for the first interface must succeed.

</li>
<li>
It must be transitive â€” if a client holding a pointer to one interface queries successfully for a second, and through that pointer queries successfully for a third interface, a query for the first interface through the pointer for the third interface must succeed.

</li>
</ul>
<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementations of <b>QueryInterface</b> must never check ACLs. The main reason for this rule is that COM requires that an object supporting a particular interface always return success when queried for that interface. Another reason is that checking ACLs on <b>QueryInterface</b> does not provide any real security because any client who has access to a particular interface can hand it directly to another client without any calls back to the server. Also, because COM caches interface pointers, it does not call <b>QueryInterface</b> on the server every time a client does a query.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

