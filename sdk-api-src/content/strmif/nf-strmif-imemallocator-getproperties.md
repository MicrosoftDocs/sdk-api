---
UID: NF:strmif.IMemAllocator.GetProperties
title: IMemAllocator::GetProperties (strmif.h)
author: windows-sdk-content
description: The GetProperties method retrieves the number of buffers that the allocator will create, and the buffer properties.
old-location: dshow\imemallocator_getproperties.htm
tech.root: DirectShow
ms.assetid: d7b7153c-24c4-4508-925b-b5cfbc26badc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [DirectShow], GetProperties method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],GetProperties method, IMemAllocator.GetProperties, IMemAllocator::GetProperties, IMemAllocatorGetProperties, dshow.imemallocator_getproperties, strmif/IMemAllocator::GetProperties
ms.topic: method
f1_keywords: 
 - "strmif/IMemAllocator.GetProperties"
dev_langs:
 - c++
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
 - IMemAllocator.GetProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemAllocator::GetProperties


## -description



The <code>GetProperties</code> method retrieves the number of buffers that the allocator will create, and the buffer properties.




## -parameters




### -param pProps [out]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-allocator_properties">ALLOCATOR_PROPERTIES</a> structure that receives the allocator properties.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



Calls to this method might not succeed until the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>
 

 

