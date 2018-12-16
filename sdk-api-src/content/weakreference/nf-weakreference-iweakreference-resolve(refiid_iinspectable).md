---
UID: NF:weakreference.IWeakReference.Resolve(REFIID,IInspectable)
title: IWeakReference::Resolve(REFIID,IInspectable)
author: windows-sdk-content
description: Resolves a weak reference by returning a strong reference to the specified object.
old-location: winrt\iweakreference_resolve.htm
tech.root: WinRT
ms.assetid: 642e44f1-7090-4391-b56c-9ba203c30e37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWeakReference interface [Windows Runtime],Resolve method, IWeakReference.Resolve, IWeakReference.Resolve(REFIID,IInspectable), IWeakReference::Resolve, IWeakReference::Resolve(REFIID,IInspectable), Resolve, Resolve method [Windows Runtime], Resolve method [Windows Runtime],IWeakReference interface, weakreference/IWeakReference::Resolve, winrt.iweakreference_resolve
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

The strong reference to the specified object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you try to resolve a weak reference to a strong reference for an object that is no longer available, <b>IWeakReference::Resolve</b> returns <b>S_OK</b>, but the <i>objectReference</i> parameter points to null.




## -see-also




<a href="https://msdn.microsoft.com/fae8bf21-2a38-4e98-9a11-89c548da9e95">IWeakReference</a>
 

 

