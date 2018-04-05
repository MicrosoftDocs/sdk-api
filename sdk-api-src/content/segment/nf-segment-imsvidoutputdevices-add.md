---
UID: NF:segment.IMSVidOutputDevices.Add
title: IMSVidOutputDevices::Add method
author: windows-driver-content
description: The Add method adds an output device to the collection.
old-location: mstv\imsvidoutputdevices_add.htm
old-project: mstv
ms.assetid: 4f8386bb-5494-4534-adec-d37ac105a3a4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies], IMSVidOutputDevices interface, Add,IMSVidOutputDevices.Add, IMSVidOutputDevices, IMSVidOutputDevices interface [Microsoft TV Technologies], Add method, IMSVidOutputDevices::Add, IMSVidOutputDevicesAdd, mstv.imsvidoutputdevices_add, segment/IMSVidOutputDevices::Add
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
-	IMSVidOutputDevices.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidOutputDevices::Add method


## -description


The <b>Add</b> method adds an output device to the collection.


## -parameters




### -param pDB [in]

Specifies a pointer to the device's <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a> interface.


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




<a href="https://msdn.microsoft.com/54776225-ad60-450b-99b4-851cae60ffa7">IMSVidOutputDevices Interface</a>



<a href="https://msdn.microsoft.com/40c4bc6b-091b-44b5-a313-5db20842adcf">IMSVidOutputDevices::Remove</a>
 

 

