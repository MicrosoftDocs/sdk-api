---
UID: NN:weakreference.IWeakReferenceSource
title: IWeakReferenceSource (weakreference.h)
description: Represents a source object to which a weak reference can be retrieved.
helpviewer_keywords: ["IWeakReferenceSource","IWeakReferenceSource interface [Windows Runtime]","IWeakReferenceSource interface [Windows Runtime]","described","weakreference/IWeakReferenceSource","winrt.iweakreferencesource"]
old-location: winrt\iweakreferencesource.htm
tech.root: WinRT
ms.assetid: f4b85374-192b-4024-80c2-a46bfebb16c1
ms.date: 12/05/2018
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
 - IWeakReferenceSource
 - weakreference/IWeakReferenceSource
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
 - IWeakReferenceSource
---

## -description

Represents a source object to which a weak reference can be retrieved.

> [!NOTE]
> With only a few exceptions, weak reference support is on by default for Windows Runtime types that you consume or author in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/), WRL, and C++/CX. **Windows.UI.Composition** and **Windows.Devices.Input.PenDevice** are examples of exceptions&mdash;that is, namespaces where weak reference support is *not* on for those types.
> 
> If you're authoring types, then see [Weak references in C++/WinRT](/windows/uwp/cpp-and-winrt-apis/weak-references#weak-references-in-cwinrt).

## -inheritance

The <b>IWeakReferenceSource</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.
