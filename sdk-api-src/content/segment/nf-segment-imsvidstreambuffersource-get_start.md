---
UID: NF:segment.IMSVidStreamBufferSource.get_Start
title: IMSVidStreamBufferSource::get_Start
author: windows-sdk-content
description: The get_Start method retrieves the start time.
old-location: mstv\imsvidstreambuffersource_get_start.htm
tech.root: mstv
ms.assetid: 4c6ad8b7-93d9-46de-b84a-a4575f3e6183
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],get_Start method, IMSVidStreamBufferSource.get_Start, IMSVidStreamBufferSource::get_Start, IMSVidStreamBufferSourceget_Start, get_Start, get_Start method [Microsoft TV Technologies], get_Start method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_get_start, segment/IMSVidStreamBufferSource::get_Start
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
 - IMSVidStreamBufferSource.get_Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSource::get_Start


## -description


The <b>get_Start</b> method retrieves the start time.


## -parameters




### -param lStart [out]

Pointer to a variable that receives the start time, in hundredths of seconds.


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
 

 

