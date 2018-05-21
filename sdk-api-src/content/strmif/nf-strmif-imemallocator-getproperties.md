---
UID: NF:strmif.IMemAllocator.GetProperties
title: IMemAllocator::GetProperties
author: windows-driver-content
description: The GetProperties method retrieves the number of buffers that the allocator will create, and the buffer properties.
old-location: dshow\imemallocator_getproperties.htm
old-project: DirectShow
ms.assetid: d7b7153c-24c4-4508-925b-b5cfbc26badc
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetProperties, GetProperties method [DirectShow], GetProperties method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],GetProperties method, IMemAllocator.GetProperties, IMemAllocator::GetProperties, IMemAllocatorGetProperties, dshow.imemallocator_getproperties, strmif/IMemAllocator::GetProperties
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMemAllocator.GetProperties
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocator::GetProperties


## -description



The <code>GetProperties</code> method retrieves the number of buffers that the allocator will create, and the buffer properties.




## -parameters




### -param pProps [out]

Pointer to an <a href="https://msdn.microsoft.com/813e4693-b549-4045-aff5-08f2dd754b6e">ALLOCATOR_PROPERTIES</a> structure that receives the allocator properties.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



Calls to this method might not succeed until the <a href="https://msdn.microsoft.com/34db4c1f-5642-4495-a572-9a78b1ee7b7e">IMemAllocator::Commit</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator Interface</a>
 

 

