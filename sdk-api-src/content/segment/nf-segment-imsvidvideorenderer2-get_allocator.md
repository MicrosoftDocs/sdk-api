---
UID: NF:segment.IMSVidVideoRenderer2.get_Allocator
title: IMSVidVideoRenderer2::get_Allocator (segment.h)
author: windows-sdk-content
description: The get_Allocator method retrieves the allocator-presenter from the VMR as an IUnknown pointer.
old-location: mstv\imsvidvideorenderer2_get_allocator.htm
tech.root: mstv
ms.assetid: 0ba2c9ba-c3ba-4095-8221-a424776f3fac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],get_Allocator method, IMSVidVideoRenderer2.get_Allocator, IMSVidVideoRenderer2::get_Allocator, IMSVidVideoRenderer2get_Allocator, get_Allocator, get_Allocator method [Microsoft TV Technologies], get_Allocator method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_get_allocator, segment/IMSVidVideoRenderer2::get_Allocator
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
 - IMSVidVideoRenderer2.get_Allocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer2::get_Allocator


## -description


The <b>get_Allocator</b> method retrieves the allocator-presenter from the VMR as an <b>IUnknown</b> pointer.

This method is provided for Automation clients. C++ applications can also use the <a href="https://msdn.microsoft.com/en-us/library/Dd694717(v=VS.85).aspx">get__Allocator</a> method, which returns an <a href="https://msdn.microsoft.com/en-us/library/Dd390499(v=VS.85).aspx">IVMRSurfaceAllocator</a> pointer.


## -parameters




### -param AllocPresent [out]

Receives a pointer to the allocator-presenter's <b>IUnknown</b> interface.


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
</table>
 




## -remarks



The caller must release the returned <b>IUnknown</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694713(v=VS.85).aspx">IMSVidVideoRenderer2 Interface</a>
 

 

