---
UID: NF:strmif.IMemInputPin.GetAllocator
title: IMemInputPin::GetAllocator
author: windows-sdk-content
description: The GetAllocator method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.
old-location: dshow\imeminputpin_getallocator.htm
tech.root: DirectShow
ms.assetid: ab49028e-ae27-4d4e-a5f1-a086ade25c5e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetAllocator, GetAllocator method [DirectShow], GetAllocator method [DirectShow],IMemInputPin interface, IMemInputPin interface [DirectShow],GetAllocator method, IMemInputPin.GetAllocator, IMemInputPin::GetAllocator, IMemInputPinGetAllocator, dshow.imeminputpin_getallocator, strmif/IMemInputPin::GetAllocator
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMemInputPin.GetAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMemInputPin::GetAllocator


## -description



The <code>GetAllocator</code> method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.




## -parameters




### -param ppAllocator [out]

Receives a pointer to the allocator's <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> interface. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_ALLOCATOR</b></dt>
</dl>
</td>
<td width="60%">
No allocator is available.

</td>
</tr>
</table>
 




## -remarks



When an output pin connects to an input pin, it negotiates with the input pin to decide on a memory allocator. The output pin calls this method to retrieve the input pin's proposed allocator. It calls the <a href="https://msdn.microsoft.com/dbc9c0ce-3e9c-4402-9d3e-1c7295e94ad9">IMemInputPin::NotifyAllocator</a> method to specify which allocator it selected.

If this method succeeds, the <b>IMemAllocator</b> interface has an outstanding reference count. Be sure to release it when you are done.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 

