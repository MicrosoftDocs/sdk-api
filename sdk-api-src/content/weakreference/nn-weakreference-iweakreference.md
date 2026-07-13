---
UID: NN:weakreference.IWeakReference
title: IWeakReference (weakreference.h)
description: Represents a weak reference to an object.
helpviewer_keywords: ["IWeakReference","IWeakReference interface [Windows Runtime]","IWeakReference interface [Windows Runtime]","described","weakreference/IWeakReference","winrt.iweakreference"]
old-location: winrt\iweakreference.htm
tech.root: WinRT
ms.assetid: fae8bf21-2a38-4e98-9a11-89c548da9e95
ms.date: 12/05/2018
ms.keywords: IWeakReference, IWeakReference interface [Windows Runtime], IWeakReference interface [Windows Runtime],described, weakreference/IWeakReference, winrt.iweakreference
req.header: weakreference.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WeakReference.idl
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
 - IWeakReference
 - weakreference/IWeakReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WeakReference.h
api_name:
 - IWeakReference
---

## -description

Represents a weak reference to an object.

> [!NOTE]
> With only a few exceptions, weak reference support is on by default for Windows Runtime types that you consume or author in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/), WRL, and C++/CX. **Windows.UI.Composition** and **Windows.Devices.Input.PenDevice** are examples of exceptions&mdash;that is, namespaces where weak reference support is *not* on for those types.
> 
> If you're authoring types, then see [Weak references in C++/WinRT](/windows/uwp/cpp-and-winrt-apis/weak-references#weak-references-in-cwinrt).

## -inheritance

The <b>IWeakReference</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 
