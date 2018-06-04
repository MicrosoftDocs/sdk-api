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

# IWMCodecOutputTimestamp::GetNextOutputTime


## -description



Queries the decoder for the time stamp of the upcoming output sample. Use this method if you need to know the time of the sample before calling <b>IMediaObject::ProcessOutput</b> or <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> to get the sample.



## -parameters




### -param prtTime [out]

Address of a variable that receives the presentation time of the next sample.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



This method is important when decoding video using frame interpolation, because the rendering application cannot predict the time stamps of interpolated frames.




## -see-also




<a href="https://msdn.microsoft.com/0dbac3fa-7521-434d-aa0a-2e8422c3da59">IWMCodecOutputTimestamp Interface</a>
 

 

