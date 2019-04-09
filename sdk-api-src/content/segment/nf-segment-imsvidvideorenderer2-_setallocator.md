---
UID: NF:segment.IMSVidVideoRenderer2._SetAllocator
title: IMSVidVideoRenderer2::_SetAllocator (segment.h)
author: windows-sdk-content
description: The _SetAllocator method specifies an allocator-presenter for the VMR. Applications can use this method to provide their own custom allocator-presenter objects.
old-location: mstv\imsvidvideorenderer2__setallocator.htm
tech.root: mstv
ms.assetid: dc0983c0-440d-453a-95c9-41a859a7dd9a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],_SetAllocator method, IMSVidVideoRenderer2._SetAllocator, IMSVidVideoRenderer2::_SetAllocator, IMSVidVideoRenderer2_SetAllocator, _SetAllocator, _SetAllocator method [Microsoft TV Technologies], _SetAllocator method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2__setallocator, segment/IMSVidVideoRenderer2::_SetAllocator
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
 - IMSVidVideoRenderer2._SetAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer2::_SetAllocator


## -description


The <b>_SetAllocator</b> method specifies an allocator-presenter for the VMR. Applications can use this method to provide their own custom allocator-presenter objects.


## -parameters




### -param AllocPresent [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd390499(v=VS.85).aspx">IVMRSurfaceAllocator</a> interface of the allocator-presenter object.


### -param ID [in]

Optionally, specifies an identifier (ID) for the allocator-presenter object. The default value of -1 indicates that the <a href="https://msdn.microsoft.com/ffb9566f-1c03-4aba-a9ce-a47e42894ca0">MSVidVideoRenderer</a> object will create an ID when it builds the filter graph. In that case, the MSVidVideoRenderer object uses the lower 32 bits of the allocator-presenter's <b>IUnknown</b> interface pointer as the ID. Note that the ID is for application use; the VMR does not use it.


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694713(v=VS.85).aspx">IMSVidVideoRenderer2 Interface</a>
 

 

