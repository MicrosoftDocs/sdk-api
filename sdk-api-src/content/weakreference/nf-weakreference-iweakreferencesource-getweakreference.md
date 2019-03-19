---
UID: NF:weakreference.IWeakReferenceSource.GetWeakReference
title: IWeakReferenceSource::GetWeakReference (weakreference.h)
author: windows-sdk-content
description: Retrieves a weak reference from an IWeakReferenceSource.
old-location: winrt\iweakreferencesource_getweakreference.htm
tech.root: WinRT
ms.assetid: 6856cad0-4571-4951-a917-8d010706f2d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWeakReference, GetWeakReference method [Windows Runtime], GetWeakReference method [Windows Runtime],IWeakReferenceSource interface, IWeakReferenceSource interface [Windows Runtime],GetWeakReference method, IWeakReferenceSource.GetWeakReference, IWeakReferenceSource::GetWeakReference, weakreference/IWeakReferenceSource::GetWeakReference, winrt.iweakreferencesource_getweakreference
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
 - IWeakReferenceSource.GetWeakReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWeakReferenceSource::GetWeakReference


## -description


Retrieves a weak reference from an <a href="https://msdn.microsoft.com/f4b85374-192b-4024-80c2-a46bfebb16c1">IWeakReferenceSource</a>.


## -parameters




### -param weakReference [out, retval]

Type: <b><a href="https://msdn.microsoft.com/fae8bf21-2a38-4e98-9a11-89c548da9e95">IWeakReference</a>**</b>

The weak reference.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f4b85374-192b-4024-80c2-a46bfebb16c1">IWeakReferenceSource</a>
 

 

