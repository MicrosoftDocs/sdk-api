---
UID: NF:unknwn.IUnknown.Release
title: IUnknown::Release
description: Decrements the reference count for an interface on a COM object.
helpviewer_keywords: ["IUnknown interface [COM]","Release method","IUnknown.Release","IUnknown::Release","Release","Release method [COM]","Release method [COM]","IUnknown interface","_com_iunknown_release","com.iunknown_release","unknwn/IUnknown::Release"]
old-location: com\iunknown_release.htm
tech.root: com
ms.assetid: 4b494c6f-f0ee-4c35-ae45-ed956f40dc7a
ms.date: 05/31/2019
ms.keywords: IUnknown interface [COM],Release method, IUnknown.Release, IUnknown::Release, Release, Release method [COM], Release method [COM],IUnknown interface, _com_iunknown_release, com.iunknown_release, unknwn/IUnknown::Release
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
 - IUnknown::Release
 - unknwn/IUnknown::Release
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
 - IUnknown.Release
---

## -description

Decrements the reference count for an interface on a COM object.



## -returns

The method returns the new reference count. This value is intended to be used only for test purposes.

## -remarks

When the reference count on an object reaches zero, **Release** must cause the interface pointer to free itself. When the released pointer is the only (formerly) outstanding reference to an object (whether the object supports single or multiple interfaces), the implementation must free the object.

Note that aggregation of objects restricts the ability to recover interface pointers.

### Notes to callers

Call this method when you no longer need to use an interface pointer. If you are writing a method that takes an in-out parameter, call **Release** on the pointer you are passing in before copying the out-value on top of it.

## -see-also

* [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown)

