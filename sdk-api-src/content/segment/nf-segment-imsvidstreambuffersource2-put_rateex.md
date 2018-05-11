---
UID: NF:segment.IMSVidStreamBufferSource2.put_RateEx
title: IMSVidStreamBufferSource2::put_RateEx
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersource2_put_rateex.htm
old-project: mstv
ms.assetid: b213ad08-8a72-4b4a-bffa-b68783693340
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],put_RateEx method, IMSVidStreamBufferSource2.put_RateEx, IMSVidStreamBufferSource2::put_RateEx, IMSVidStreamBufferSource2put_RateEx, mstv.imsvidstreambuffersource2_put_rateex, put_RateEx, put_RateEx method [Microsoft TV Technologies], put_RateEx method [Microsoft TV Technologies],IMSVidStreamBufferSource2 interface, segment/IMSVidStreamBufferSource2::put_RateEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	IMSVidStreamBufferSource2.put_RateEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSource2::put_RateEx


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>put_RateEx</b> method sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").


## -parameters




### -param dwRate




### -param dwFramesPerSecond [in]

Frames per second for fast-forward play. For more information, see <a href="https://msdn.microsoft.com/37b80d0d-561d-4ef3-b0ad-70fb43530026">IStreamBufferMediaSeeking2::SetRateEx</a>.


#### - dRate [in]

Playback rate. The valid range is (<i>dRate</i> &gt;= 0.1 || <i>dRate</i> &lt;= –0.1).


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
 




## -see-also




<a href="https://msdn.microsoft.com/47012868-4c9e-4974-8549-11331836bed0">IMSVidStreamBufferSource2 Interface</a>
 

 

