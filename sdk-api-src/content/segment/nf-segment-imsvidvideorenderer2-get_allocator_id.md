---
UID: NF:segment.IMSVidVideoRenderer2.get_Allocator_ID
title: IMSVidVideoRenderer2::get_Allocator_ID
author: windows-sdk-content
description: The get_Allocator_ID method retrieves an identifier for the VMR filter's allocator-presenter.
old-location: mstv\imsvidvideorenderer2_get_allocator_id.htm
tech.root: mstv
ms.assetid: 4d512525-ed18-43af-9773-ed56c49c3641
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],get_Allocator_ID method, IMSVidVideoRenderer2.get_Allocator_ID, IMSVidVideoRenderer2::get_Allocator_ID, IMSVidVideoRenderer2get_Allocator_ID, get_Allocator_ID, get_Allocator_ID method [Microsoft TV Technologies], get_Allocator_ID method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_get_allocator_id, segment/IMSVidVideoRenderer2::get_Allocator_ID
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
 - IMSVidVideoRenderer2.get_Allocator_ID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer2::get_Allocator_ID


## -description


The <b>get_Allocator_ID</b> method retrieves an identifier for the VMR filter's allocator-presenter.


## -parameters




### -param ID [out]

Receives the identifier. If the returned value is -1, the <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">MSVidVideoRenderer</a> object will assign a default identifier when it builds the filter graph.


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



The identifier is for application use; it is not used by the VMR.




## -see-also




<a href="https://msdn.microsoft.com/caaa2cf1-15be-47dc-82db-06915a55ba03">IMSVidVideoRenderer2 Interface</a>
 

 

