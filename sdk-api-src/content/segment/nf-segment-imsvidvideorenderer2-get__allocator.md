---
UID: NF:segment.IMSVidVideoRenderer2.get__Allocator
title: IMSVidVideoRenderer2::get__Allocator
author: windows-sdk-content
description: The get__Allocator method retrieves the allocator-presenter from the VMR.
old-location: mstv\imsvidvideorenderer2_get__allocator.htm
tech.root: mstv
ms.assetid: b22d643e-f458-4293-9f2b-e8bfe1499905
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],get__Allocator method, IMSVidVideoRenderer2.get__Allocator, IMSVidVideoRenderer2::get__Allocator, IMSVidVideoRenderer2get__Allocator, get__Allocator, get__Allocator method [Microsoft TV Technologies], get__Allocator method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_get__allocator, segment/IMSVidVideoRenderer2::get__Allocator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidVideoRenderer2.get__Allocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidVideoRenderer2.get__Allocator
: 
---

# IMSVidVideoRenderer2::get__Allocator


## -description


The <b>get__Allocator</b> method retrieves the allocator-presenter from the VMR.


## -parameters




### -param AllocPresent [out]

Receives an <a href="https://msdn.microsoft.com/bbcbe152-80fd-469b-a79b-c8db6f97da22">IVMRSurfaceAllocator</a> interface pointer.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



The caller must release the <a href="https://msdn.microsoft.com/bbcbe152-80fd-469b-a79b-c8db6f97da22">IVMRSurfaceAllocator</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/caaa2cf1-15be-47dc-82db-06915a55ba03">IMSVidVideoRenderer2 Interface</a>
 

 

