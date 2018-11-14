---
UID: NF:segment.IMSVidAudioRendererDevices.get_Count
title: IMSVidAudioRendererDevices::get_Count
author: windows-sdk-content
description: The get_Count method retrieves the number of items in the collection.
old-location: mstv\imsvidaudiorendererdevices_get_count.htm
tech.root: MSTV
ms.assetid: 46a3b579-a027-4c80-9f7a-f81dd9af4d0d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidAudioRendererDevices interface [Microsoft TV Technologies],get_Count method, IMSVidAudioRendererDevices.get_Count, IMSVidAudioRendererDevices::get_Count, IMSVidAudioRendererDevicesget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IMSVidAudioRendererDevices interface, mstv.imsvidaudiorendererdevices_get_count, segment/IMSVidAudioRendererDevices::get_Count
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
 - IMSVidAudioRendererDevices.get_Count
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
- IMSVidAudioRendererDevices.get_Count
: 
---

# IMSVidAudioRendererDevices::get_Count


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




<a href="https://msdn.microsoft.com/2cf03260-7abe-4602-8364-447d076a4f76">IMSVidAudioRendererDevices Interface</a>
 

 

