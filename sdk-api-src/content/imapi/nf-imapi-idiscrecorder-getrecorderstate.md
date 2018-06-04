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

# IDiscRecorder::GetRecorderState


## -description


Retrieves the disc recorder state.


## -parameters




### -param pulDevStateFlags [out]

One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECORDER_BURNING"></a><a id="recorder_burning"></a><dl>
<dt><b>RECORDER_BURNING</b></dt>
</dl>
</td>
<td width="60%">
0x2

</td>
</tr>
<tr>
<td width="40%"><a id="RECORDER_DOING_NOTHING"></a><a id="recorder_doing_nothing"></a><dl>
<dt><b>RECORDER_DOING_NOTHING</b></dt>
</dl>
</td>
<td width="60%">
0x0

</td>
</tr>
<tr>
<td width="40%"><a id="RECORDER_OPENED"></a><a id="recorder_opened"></a><dl>
<dt><b>RECORDER_OPENED</b></dt>
</dl>
</td>
<td width="60%">
0x1

</td>
</tr>
</table>
 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

