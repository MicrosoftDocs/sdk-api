---
UID: NF:strmif.IMemInputPin.NotifyAllocator
title: IMemInputPin::NotifyAllocator (strmif.h)
author: windows-sdk-content
description: The NotifyAllocator method specifies an allocator for the connection.
old-location: dshow\imeminputpin_notifyallocator.htm
tech.root: DirectShow
ms.assetid: dbc9c0ce-3e9c-4402-9d3e-1c7295e94ad9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMemInputPin interface [DirectShow],NotifyAllocator method, IMemInputPin.NotifyAllocator, IMemInputPin::NotifyAllocator, IMemInputPinNotifyAllocator, NotifyAllocator, NotifyAllocator method [DirectShow], NotifyAllocator method [DirectShow],IMemInputPin interface, dshow.imeminputpin_notifyallocator, strmif/IMemInputPin::NotifyAllocator
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemInputPin.NotifyAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemInputPin::NotifyAllocator


## -description



The <code>NotifyAllocator</code> method specifies an allocator for the connection.




## -parameters




### -param pAllocator [in]

Pointer to the allocator's <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> interface.


### -param bReadOnly [out]

Flag that specifies whether samples from this allocator are read-only. If <b>TRUE</b>, samples are read-only.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin. The output pin might use the allocator that the input pin proposed in the <a href="https://msdn.microsoft.com/ab49028e-ae27-4d4e-a5f1-a086ade25c5e">IMemInputPin::GetAllocator</a> method, or it might provide its own allocator.

If the <i>bReadOnly</i> parameter is <b>TRUE</b>, all samples in the allocator are read-only. The filter must copy them to modify the data.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 

