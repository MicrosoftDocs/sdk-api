---
UID: NF:unknwn.IUnknown.QueryInterface(REFIID,void)
title: IUnknown::QueryInterface(REFIID,void)
description: Retrieves pointers to the supported interfaces on an object.
helpviewer_keywords: ["IUnknown interface [COM]","QueryInterface method","IUnknown.QueryInterface","IUnknown.QueryInterface(REFIID","void)","IUnknown::QueryInterface","IUnknown::QueryInterface(REFIID","void)","QueryInterface","QueryInterface method [COM]","QueryInterface method [COM]","IUnknown interface","_com_iunknown_queryinterface","com.iunknown_queryinterface","unknwn/IUnknown::QueryInterface"]
old-location: com\iunknown_queryinterface.htm
tech.root: com
ms.assetid: 54d5ff80-18db-43f2-b636-f93ac053146d
ms.date: 05/31/2019
ms.keywords: IUnknown interface [COM],QueryInterface method, IUnknown.QueryInterface, IUnknown.QueryInterface(REFIID,void), IUnknown::QueryInterface, IUnknown::QueryInterface(REFIID,void), QueryInterface, QueryInterface method [COM], QueryInterface method [COM],IUnknown interface, _com_iunknown_queryinterface, com.iunknown_queryinterface, unknwn/IUnknown::QueryInterface
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnknown::QueryInterface
 - unknwn/IUnknown::QueryInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Unknwn.h
api_name:
 - IUnknown.QueryInterface
---

## -description

Queries a COM object for a pointer to one of its interface; identifying the interface by a reference to its interface identifier (IID). If the COM object implements the interface, then it returns a pointer to that interface after calling [IUnknown::AddRef](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) on it.

## -parameters

### -param riid

Type: **REFIID**

A reference to the interface identifier (IID) of the interface being queried for.

### -param ppvObject

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

The address of a pointer to an interface with the IID specified in the *riid* parameter. Because you pass the address of an interface pointer, the method can overwrite that address with the pointer to the interface being queried for. Upon successful return, *\*ppvObject* (the dereferenced address) contains a pointer to the requested interface. If the object doesn't support the interface, the method sets *\*ppvObject* (the dereferenced address) to `nullptr`.

## -returns

This method returns **S_OK** if the interface is supported, and **E_NOINTERFACE** otherwise. If *ppvObject* (the address) is `nullptr`, then this method returns **E_POINTER**.

## -remarks

For any given COM object (also known as a COM component), a specific query for the [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown) on any of the object's interfaces must always return the same pointer value. This enables a client to determine whether two pointers point to the same component by calling **QueryInterface** with **IID_IUnknown** and comparing the results. It is specifically not the case that queries for interfaces other than **IUnknown** (even the same interface through the same pointer) must return the same pointer value.

There are four requirements for implementations of **QueryInterface** (In these cases, "must succeed" means "must succeed barring catastrophic failure.").

- The set of interfaces accessible on an object through **QueryInterface** must be static, not dynamic. This means that if a call to **QueryInterface** for a pointer to a specified interface succeeds the first time, then it must succeed again. If the call fails the first time, then it must fail on all subsequent calls.
- It must be reflexive&mdash;if a client holds a pointer to an interface on an object, and the client queries for that interface, then the call must succeed.
- It must be symmetric&mdash;if a client holding a pointer to one interface queries successfully for another, then a query through the obtained pointer for the first interface must succeed.
- It must be transitive&mdash;if a client holding a pointer to one interface queries successfully for a second, and through that pointer queries successfully for a third interface, then a query for the first interface through the pointer for the third interface must succeed.

### Notes to implementers

Implementations of **QueryInterface** must never check ACLs. The main reason for this rule is that COM requires that an object supporting a particular interface always return success when queried for that interface. Another reason is that checking ACLs on **QueryInterface** does not provide any real security because any client who has access to a particular interface can hand it directly to another client without any calls back to the server. Also, because COM caches interface pointers, it does not call **QueryInterface** on the server every time a client does a query.

## -see-also

* [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown)

