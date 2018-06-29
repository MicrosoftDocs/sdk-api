---
UID: NF:sbe.IStreamBufferMediaSeeking2.SetRateEx
title: IStreamBufferMediaSeeking2::SetRateEx
author: windows-sdk-content
description: "."
old-location: mstv\istreambuffermediaseeking2_setrateex.htm
old-project: mstv
ms.assetid: 37b80d0d-561d-4ef3-b0ad-70fb43530026
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies],SetRateEx method, IStreamBufferMediaSeeking2.SetRateEx, IStreamBufferMediaSeeking2::SetRateEx, IStreamBufferMediaSeeking2SetRateEx, SetRateEx, SetRateEx method [Microsoft TV Technologies], SetRateEx method [Microsoft TV Technologies],IStreamBufferMediaSeeking2 interface, mstv.istreambuffermediaseeking2_setrateex, sbe/IStreamBufferMediaSeeking2::SetRateEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
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
 - IStreamBufferMediaSeeking2.SetRateEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferMediaSeeking2::SetRateEx


## -description




The <b>SetRateEx</b> method sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").


## -parameters




### -param dRate [in]

Playback rate. Valid range is (<i>dRate</i> &gt;= 0.1 || <i>dRate</i> &lt;= -0.1).


### -param dwFramesPerSec [in]

Frames per second for fast-forward play. Cannot be zero. See Remarks for more information.


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



At higher frames rates, the Stream Buffer Engine drops delta frames and may skip some key frames. This behavior is determined by the <a href="https://msdn.microsoft.com/c6e7b27a-b217-4430-adf7-c7ebc7e17bf6">IStreamBufferConfigure2::SetFFTransitionRates</a> method. When the playback rate exceeds the value given in that method's <i>dwMaxNonSkippingRate</i> parameter, the Stream Buffer Engine starts to skip key frames. The number of skipped key frames is determined by the playback rate. To control how many key frames are skipped, use the <b>SetRateEx</b> method:

<ul>
<li>If the playback rate is less than or equal to <i>dwMaxNonSkippingRate</i>, the <i>dwFramesPerSec</i> parameter is ignored.</li>
<li>If the playback rate exceeds <i>dwMaxNonSkippingRate</i>, the Stream Buffer Engine maintains the frame rate specified in <i>dwFramesPerSec</i> and drops key frames if necessary.</li>
</ul>
The frame rate is applied to the video stream. If there is no video stream, the method fails. The actual frame rate may vary over short periods of time.




## -see-also




<a href="https://msdn.microsoft.com/3029868e-0b27-4ce9-90b2-22d8e1961a1f">IStreamBufferMediaSeeking2 Interface</a>
 

 

