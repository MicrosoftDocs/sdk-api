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

# IStreamBufferConfigure2::SetFFTransitionRates


## -description


The <b>SetFFTransitionRates</b> method sets the behavior of fast-forward play ("trick mode") in the Stream Buffer Engine.


## -parameters




### -param dwMaxFullFrameRate [in]

Maximum playback rate for full-frame playback. The value must be greater than 1. The default value is 4.


### -param dwMaxNonSkippingRate [in]

Maximum playback rate for key-frame playback. The value must be greater than <i>dwFullFrameRate</i>. The default value is 6.


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



At higher playback rates, the Stream Buffer Engine drops frames in order to maintain the desired rate. The following table shows how the values of <i>dwMaxFullFrameRate</i> and <i>dwMaxNonSkippingRate</i> affect playback.

<table>
<tr>
<th>
              Playback rate
            </th>
<th>
              Behavior
            </th>
</tr>
<tr>
<td>rate &lt;= <i>dwMaxFullFrameRate</i></td>
<td>Full-frame playback: All frames are sent.</td>
</tr>
<tr>
<td><i>dwMaxFullFrameRate</i> &lt; rate &lt;= <i>dwMaxNonSkippingRate</i></td>
<td>Key-frame playback: All key frames are sent. Delta frames are skipped.</td>
</tr>
<tr>
<td><i>dwMaxNonSkippingRate</i> &lt; rate</td>
<td>Key-frame playback with seeking: All delta frames are skipped, and some key frames are skipped. The number of skipped key frames is proportional to the rate.</td>
</tr>
</table>
 

The decoder may drop frames as well, depending on the data rate, the monitor refresh rate, and the CPU load.




## -see-also




<a href="https://msdn.microsoft.com/df71783c-1ff3-46b0-bae2-61d12f4d70d0">IStreamBufferConfigure2 Interface</a>



<a href="https://msdn.microsoft.com/37b80d0d-561d-4ef3-b0ad-70fb43530026">IStreamBufferMediaSeeking2::SetRateEx</a>
 

 

