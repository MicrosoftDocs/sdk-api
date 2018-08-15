---
UID: NF:strmif.IMemAllocator.SetProperties
title: IMemAllocator::SetProperties
author: windows-sdk-content
description: The SetProperties method specifies the number of buffers to allocate and the size of each buffer.
old-location: dshow\imemallocator_setproperties.htm
old-project: DirectShow
ms.assetid: c68f2e2f-c70f-447d-804b-dfdfe8ae8a52
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMemAllocator interface [DirectShow],SetProperties method, IMemAllocator.SetProperties, IMemAllocator::SetProperties, IMemAllocatorSetProperties, SetProperties, SetProperties method [DirectShow], SetProperties method [DirectShow],IMemAllocator interface, dshow.imemallocator_setproperties, strmif/IMemAllocator::SetProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocator.SetProperties
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocator::SetProperties


## -description



The <code>SetProperties</code> method specifies the number of buffers to allocate and the size of each buffer.




## -parameters




### -param pRequest

Pointer to an <a href="https://msdn.microsoft.com/813e4693-b549-4045-aff5-08f2dd754b6e">ALLOCATOR_PROPERTIES</a> structure that contains the buffer requirements.


### -param pActual

Pointer to an <b>ALLOCATOR_PROPERTIES</b> structure that receives the actual buffer properties.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ALREADY_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot change allocated memory while the filter is active.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
An invalid alignment was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BUFFERS_OUTSTANDING</b></dt>
</dl>
</td>
<td width="60%">
One or more buffers are still active.

</td>
</tr>
</table>
 




## -remarks



This method specifies the buffer requirements, but does not allocate any buffers. Call the <a href="https://msdn.microsoft.com/34db4c1f-5642-4495-a572-9a78b1ee7b7e">IMemAllocator::Commit</a> method to allocate buffers.

The caller allocates two ALLOCATOR_PROPERTIES structures. The <i>pRequest</i> parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer. When the method returns, the <i>pActual</i> parameter contains the actual buffer properties, as set by the allocator.

When this method is called, the allocator must not be committed or have outstanding buffers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator Interface</a>
 

 

