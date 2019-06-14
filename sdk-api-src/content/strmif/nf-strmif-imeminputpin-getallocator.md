---
UID: NF:strmif.IMemInputPin.GetAllocator
title: IMemInputPin::GetAllocator (strmif.h)
author: windows-sdk-content
description: The GetAllocator method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.
old-location: dshow\imeminputpin_getallocator.htm
tech.root: DirectShow
ms.assetid: ab49028e-ae27-4d4e-a5f1-a086ade25c5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllocator, GetAllocator method [DirectShow], GetAllocator method [DirectShow],IMemInputPin interface, IMemInputPin interface [DirectShow],GetAllocator method, IMemInputPin.GetAllocator, IMemInputPin::GetAllocator, IMemInputPinGetAllocator, dshow.imeminputpin_getallocator, strmif/IMemInputPin::GetAllocator
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
ms.custom: 19H1
---

# IMemInputPin::GetAllocator


## -description



The <code>GetAllocator</code> method retrieves the memory allocator proposed by this pin. After the allocator has been selected, this method returns a pointer to the selected allocator.




## -parameters




### -param ppAllocator [out]

Receives a pointer to the allocator's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface. The caller must release the interface.


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



When an output pin connects to an input pin, it negotiates with the input pin to decide on a memory allocator. The output pin calls this method to retrieve the input pin's proposed allocator. It calls the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-notifyallocator">IMemInputPin::NotifyAllocator</a> method to specify which allocator it selected.

If this method succeeds, the <b>IMemAllocator</b> interface has an outstanding reference count. Be sure to release it when you are done.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>
 

 

