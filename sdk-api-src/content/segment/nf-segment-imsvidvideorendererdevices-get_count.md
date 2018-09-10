---
UID: NF:segment.IMSVidVideoRendererDevices.get_Count
title: IMSVidVideoRendererDevices::get_Count
author: windows-sdk-content
description: The get_Count method retrieves the number of items in the collection.
old-location: mstv\imsvidvideorendererdevices_get_count.htm
tech.root: mstv
ms.assetid: 4308ed6a-b9c4-46f3-98eb-be23cd49c7dc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidVideoRendererDevices interface [Microsoft TV Technologies],get_Count method, IMSVidVideoRendererDevices.get_Count, IMSVidVideoRendererDevices::get_Count, IMSVidVideoRendererDevicesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, mstv.imsvidvideorendererdevices_get_count, segment/IMSVidVideoRendererDevices::get_Count
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IMSVidVideoRendererDevices.get_Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRendererDevices::get_Count


## -description


The <b>get_Count</b> method retrieves the number of items in the collection.


## -parameters




### -param lCount

TBD




#### - plCount [out]

Pointer to a variable that receives the number of items.


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
 




## -see-also




<a href="https://msdn.microsoft.com/cf8e1307-b4a5-464b-b9a6-32c195941309">IMSVidVideoRendererDevices Interface</a>
 

 

