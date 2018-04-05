---
UID: NF:segment.IMSVidStreamBufferSource.put_UnratedDelay
title: IMSVidStreamBufferSource::put_UnratedDelay method
author: windows-driver-content
description: The put_UnratedDelay method specifies how long the Video Control will play unrated content before blocking it. The value is ignored until the put_BlockUnrated method is called with the value VARIANT_TRUE.
old-location: mstv\imsvidstreambuffersource_put_unrateddelay.htm
old-project: mstv
ms.assetid: 7b4e1ac4-dfb8-45c0-9079-16f8babcb494
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferSource, IMSVidStreamBufferSource interface [Microsoft TV Technologies], put_UnratedDelay method, IMSVidStreamBufferSource::put_UnratedDelay, IMSVidStreamBufferSourceput_UnratedDelay, mstv.imsvidstreambuffersource_put_unrateddelay, put_UnratedDelay method [Microsoft TV Technologies], put_UnratedDelay method [Microsoft TV Technologies], IMSVidStreamBufferSource interface, put_UnratedDelay,IMSVidStreamBufferSource.put_UnratedDelay, segment/IMSVidStreamBufferSource::put_UnratedDelay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSource.put_UnratedDelay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferSource::put_UnratedDelay method


## -description


The <b>put_UnratedDelay</b> method specifies how long the Video Control will play unrated content before blocking it. The value is ignored until the <a href="https://msdn.microsoft.com/9dd59b87-708b-4003-9575-54a02b97c272">put_BlockUnrated</a> method is called with the value VARIANT_TRUE.


## -parameters




### -param dwDelay [in]

Specifies the delay before blocking unrated content, in milliseconds.


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
 




## -see-also




<a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource Interface</a>



<a href="https://msdn.microsoft.com/9dd59b87-708b-4003-9575-54a02b97c272">IMSVidStreamBufferSource::put_BlockUnrated</a>
 

 

