---
UID: NF:segment.IMSVidVideoRenderer2.SetAllocator
title: IMSVidVideoRenderer2::SetAllocator
author: windows-sdk-content
description: The SetAllocator method specifies an allocator-presenter for the VMR. Applications can use this method to provide their own custom allocator-presenter objects.
old-location: mstv\imsvidvideorenderer2_setallocator.htm
tech.root: MSTV
ms.assetid: c73edfea-bafd-4640-9be6-45e5a2bb81ef
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],SetAllocator method, IMSVidVideoRenderer2.SetAllocator, IMSVidVideoRenderer2::SetAllocator, SetAllocator, SetAllocator method [Microsoft TV Technologies], SetAllocator method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_setallocator, segment/IMSVidVideoRenderer2::SetAllocator
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
 - IMSVidVideoRenderer2.SetAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer2::SetAllocator


## -description


The <b>SetAllocator</b> method specifies an allocator-presenter for the VMR. Applications can use this method to provide their own custom allocator-presenter objects.


## -parameters




### -param AllocPresent

TBD


### -param ID [in]

Optionally, specifies an identifier (ID) for the allocator-presenter object. The default value of -1 indicates that the <a href="https://msdn.microsoft.com/ffb9566f-1c03-4aba-a9ce-a47e42894ca0">MSVidVideoRenderer</a> object will create an ID when it builds the filter graph. In that case, the MSVidVideoRenderer object uses the lower 32 bits of the allocator-presenter's <b>IUnknown</b> interface pointer as the ID. Note that the ID is for application use; the VMR does not use it.


#### - pAllocPresent [in]

Pointer to the <b>IUnknown</b> interface of the allocator-presenter object.



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




<a href="https://msdn.microsoft.com/caaa2cf1-15be-47dc-82db-06915a55ba03">IMSVidVideoRenderer2 Interface</a>
 

 

