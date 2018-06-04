---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFSeekInfo::GetNearestKeyFrames


## -description


For a particular seek position, gets the two nearest key frames.


## -parameters




### -param pguidTimeFormat [in]

A pointer to a GUID that specifies the time format. The time format defines the units for the other parameters of this method. If the value is <b>GUID_NULL</b>, the time format is 100-nanosecond units. Some media sources might support additional time format GUIDs. 


### -param pvarStartPosition [in]

The seek position. The units for this parameter are specified by <i>pguidTimeFormat</i>.


### -param pvarPreviousKeyFrame [out]

Receives the position of the nearest key frame that appears earlier than <i>pvarStartPosition</i>. The units for this parameter are specified by <i>pguidTimeFormat</i>.


### -param pvarNextKeyFrame [out]

Receives the position of the nearest key frame that appears earlier than <i>pvarStartPosition</i>. The units for this parameter are specified by <i>pguidTimeFormat</i>.


## -returns



This method can return one of these values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_TIME_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The time format specified in <i>pguidTimeFormat</i> is not supported.

</td>
</tr>
</table>
 




## -remarks



If an application seeks to a non–key frame, the decoder must start decoding from the previous key frame. This can increase latency, because several frames might get decoded before the requested frame is reached. To reduce latency, an application can call this method to find the two key frames that are closest to the desired time, and then seek to one of those key frames. 




## -see-also




<a href="https://msdn.microsoft.com/5B1AD3A1-D5ED-4F9D-A895-0312E6EB3072">IMFSeekInfo</a>
 

 

