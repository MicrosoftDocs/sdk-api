---
UID: NF:segment.IMSVidVideoRendererDevices.Add
title: IMSVidVideoRendererDevices::Add
author: windows-driver-content
description: The Add method adds a video renderer to the collection.
old-location: mstv\imsvidvideorendererdevices_add.htm
old-project: mstv
ms.assetid: 650b7895-4e4b-494a-bc06-dafb67fca391
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, IMSVidVideoRendererDevices interface [Microsoft TV Technologies],Add method, IMSVidVideoRendererDevices.Add, IMSVidVideoRendererDevices::Add, IMSVidVideoRendererDevicesAdd, mstv.imsvidvideorendererdevices_add, segment/IMSVidVideoRendererDevices::Add
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRendererDevices.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRendererDevices::Add


## -description


The <b>Add</b> method adds a video renderer to the collection.


## -parameters




### -param pDB [in]

Specifies a pointer to the video renderer's <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only; cannot add any items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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
 

 

