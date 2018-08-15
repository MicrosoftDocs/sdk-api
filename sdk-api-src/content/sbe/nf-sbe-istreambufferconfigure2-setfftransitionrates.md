---
UID: NF:sbe.IStreamBufferConfigure2.SetFFTransitionRates
title: IStreamBufferConfigure2::SetFFTransitionRates
author: windows-sdk-content
description: The SetFFTransitionRates method sets the behavior of fast-forward play (&#0034;trick mode&#0034;) in the Stream Buffer Engine.
old-location: mstv\istreambufferconfigure2_setfftransitionrates.htm
old-project: mstv
ms.assetid: c6e7b27a-b217-4430-adf7-c7ebc7e17bf6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IStreamBufferConfigure2 interface [Microsoft TV Technologies],SetFFTransitionRates method, IStreamBufferConfigure2.SetFFTransitionRates, IStreamBufferConfigure2::SetFFTransitionRates, IStreamBufferConfigure2SetFFTransitionRates, SetFFTransitionRates, SetFFTransitionRates method [Microsoft TV Technologies], SetFFTransitionRates method [Microsoft TV Technologies],IStreamBufferConfigure2 interface, mstv.istreambufferconfigure2_setfftransitionrates, sbe/IStreamBufferConfigure2::SetFFTransitionRates
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure2.SetFFTransitionRates
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
<th>Playback rate
            </th>
<th>Behavior
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
 

 

