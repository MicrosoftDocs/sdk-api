---
UID: NF:weakreference.IWeakReference.Resolve(REFIID,IInspectable)
title: IWeakReference::Resolve(REFIID,IInspectable) (weakreference.h)
description: Resolves a weak reference by returning a strong reference to the specified object.
helpviewer_keywords: ["IWeakReference interface [Windows Runtime]","Resolve method","IWeakReference.Resolve","IWeakReference.Resolve(REFIID","IInspectable)","IWeakReference::Resolve","IWeakReference::Resolve(REFIID","IInspectable)","Resolve","Resolve method [Windows Runtime]","Resolve method [Windows Runtime]","IWeakReference interface","weakreference/IWeakReference::Resolve","winrt.iweakreference_resolve"]
old-location: winrt\iweakreference_resolve.htm
tech.root: WinRT
ms.assetid: 642e44f1-7090-4391-b56c-9ba203c30e37
ms.date: 12/05/2018
ms.keywords: IWeakReference interface [Windows Runtime],Resolve method, IWeakReference.Resolve, IWeakReference.Resolve(REFIID,IInspectable), IWeakReference::Resolve, IWeakReference::Resolve(REFIID,IInspectable), Resolve, Resolve method [Windows Runtime], Resolve method [Windows Runtime],IWeakReference interface, weakreference/IWeakReference::Resolve, winrt.iweakreference_resolve
f1_keywords:
- weakreference/IWeakReference.Resolve
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WeakReference.h
api_name:
- IWeakReference.Resolve
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWeakReference::Resolve(REFIID,IInspectable)


## -description


Resolves a weak reference by returning a strong reference to the specified object.


## -parameters




### -param riid

TBD


### -param objectReference [in]

Type: <b>REFIID</b>

The reference ID of the specified object.


#### - arg2 [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

The strong reference to the specified object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you try to resolve a weak reference to a strong reference for an object that is no longer available, <b>IWeakReference::Resolve</b> returns <b>S_OK</b>, but the <i>objectReference</i> parameter points to null.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/weakreference/nn-weakreference-iweakreference">IWeakReference</a>
 

 

