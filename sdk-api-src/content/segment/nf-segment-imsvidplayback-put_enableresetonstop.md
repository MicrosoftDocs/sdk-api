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

# IMSVidPlayback::put_EnableResetOnStop


## -description


The <b>put_EnableResetOnStop</b> method indicates how playback will resume if the graph is rebuilt.


## -parameters




### -param newVal [in]

Specifies one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>VARIANT_FALSE</b></td>
<td>The Video Control attempts to start from position where playback was interrupted. (Default)</td>
</tr>
<tr>
<td><b>VARIANT_TRUE</b></td>
<td>The Video Control seeks back to the start before resuming playback.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

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
</table>
 




## -remarks



In some situations, the filter graph may be torn down and rebuilt during play. For example, this can happen if the monitor resolution changes or the screen saver starts. The <b>put_EnableResetOnStop</b> property specifies whether the Video Control should resume playback where it was interrupted, or should restart at the beginning of the source.

By default, playback resumes from the point where it was interrupted. If <i>newVal</i> is VARIANT_TRUE, however, the Video Control will issue a seek command back to time zero. Note that setting this parameter to VARIANT_TRUE does not guarantee that the seek command will succeed. The seek command might fail, depending on the source.




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

