---
UID: NF:segment.IMSVidAudioRendererDevices.Add
title: IMSVidAudioRendererDevices::Add
author: windows-sdk-content
description: The Add method adds an audio renderer to the collection.
old-location: mstv\imsvidaudiorendererdevices_add.htm
tech.root: mstv
ms.assetid: 663ca24a-9f27-4642-b8e1-901f93090bd7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IMSVidAudioRendererDevices interface, IMSVidAudioRendererDevices interface [Microsoft TV Technologies],Add method, IMSVidAudioRendererDevices.Add, IMSVidAudioRendererDevices::Add, IMSVidAudioRendererDevicesAdd, mstv.imsvidaudiorendererdevices_add, segment/IMSVidAudioRendererDevices::Add
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
 - IMSVidAudioRendererDevices.Add
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
- IMSVidAudioRendererDevices.Add
: 
---

# IMSVidAudioRendererDevices::Add


## -description


The <b>Add</b> method adds an audio renderer to the collection.


## -parameters




### -param pDB [in]

Pointer to the audio renderer's <a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer</a> interface.


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




<a href="https://msdn.microsoft.com/2cf03260-7abe-4602-8364-447d076a4f76">IMSVidAudioRendererDevices Interface</a>
 

 

