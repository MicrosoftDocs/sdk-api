---
UID: NF:strmif.IMemAllocator.Decommit
title: IMemAllocator::Decommit
author: windows-sdk-content
description: The Decommit method releases the buffer memory.
old-location: dshow\imemallocator_decommit.htm
old-project: DirectShow
ms.assetid: 2c1211c1-e047-4240-b85a-9be0a9290d31
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Decommit, Decommit method [DirectShow], Decommit method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],Decommit method, IMemAllocator.Decommit, IMemAllocator::Decommit, IMemAllocatorDecommit, dshow.imemallocator_decommit, strmif/IMemAllocator::Decommit
ms.prod: windows
ms.technology: windows-sdk
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
 - IMemAllocator.Decommit
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocator::Decommit


## -description



The <code>Decommit</code> method releases the buffer memory.




## -parameters






## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



Any threads waiting in the <a href="https://msdn.microsoft.com/a5d015c8-ef15-4bac-906f-5d064fbff11f">IMemAllocator::GetBuffer</a> method return with an error. Further calls to <b>GetBuffer</b> fail, until the <a href="https://msdn.microsoft.com/34db4c1f-5642-4495-a572-9a78b1ee7b7e">IMemAllocator::Commit</a> method is called.

The purpose of the <code>Decommit</code> method is to prevent filters from getting any more samples from the allocator. Filters that already hold a reference count on a sample are not affected. After a filter releases a sample and the reference count goes to zero, however, the sample is no longer available.

The allocator may free the memory belonging to any sample with a reference count of zero. Thus, the <code>Decommit</code> method "releases" the memory in the sense that filters stop having access to it. Whether the memory actually returns to the heap depends on the implementation of the allocator. Some allocators wait until their own destructor method. However, an allocator must not leave any allocated memory behind when it deletes itself. Therefore, an allocator's destructor must wait until all of its samples are released.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator Interface</a>
 

 

