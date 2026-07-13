---
UID: NF:unknwn.IUnknown.AddRef
title: IUnknown::AddRef
description: Increments the reference count for an interface pointer to a COM object. You should call this method whenever you make a copy of an interface pointer.
helpviewer_keywords: ["AddRef","AddRef method [COM]","AddRef method [COM]","IUnknown interface","IUnknown interface [COM]","AddRef method","IUnknown.AddRef","IUnknown::AddRef","_com_iunknown_addref","com.iunknown_addref","unknwn/IUnknown::AddRef"]
old-location: com\iunknown_addref.htm
tech.root: com
ms.assetid: b4316efd-73d4-4995-b898-8025a316ba63
ms.date: 05/31/2019
ms.keywords: AddRef, AddRef method [COM], AddRef method [COM],IUnknown interface, IUnknown interface [COM],AddRef method, IUnknown.AddRef, IUnknown::AddRef, _com_iunknown_addref, com.iunknown_addref, unknwn/IUnknown::AddRef
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
 - IUnknown::AddRef
 - unknwn/IUnknown::AddRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Unknwn.h
api_name:
 - IUnknown.AddRef
---

## -description

Increments the reference count for an interface pointer to a COM object. You should call this method whenever you make a copy of an interface pointer



## -returns

The method returns the new reference count. This value is intended to be used only for test purposes.

## -remarks

A COM object uses a per-interface reference-counting mechanism to ensure that the object doesn't outlive references to it. You use **AddRef** to stabilize a copy of an interface pointer. It can also be called when the life of a cloned pointer must extend beyond the lifetime of the original pointer. The cloned pointer must be released by calling [IUnknown::Release](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) on it.

The internal reference counter that **AddRef** maintains should be a 32-bit unsigned integer.

### Notes to callers

Call this method for every new copy of an interface pointer that you make. For example, if you return a copy of a pointer from a method, then you must call **AddRef** on that pointer. You must also call **AddRef** on a pointer before passing it as an in-out parameter to a method; the method will call [IUnknown::Release](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) before copying the out-value on top of it.

## -see-also

* [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown)

