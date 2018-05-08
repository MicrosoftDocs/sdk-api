---
UID: NF:segment.IMSVidStreamBufferSink3.SetMinSeek
title: IMSVidStreamBufferSink3::SetMinSeek
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersink3_setminseek.htm
old-project: mstv
ms.assetid: 2f7a7323-c9da-47f9-95e2-dd13fc023373
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],SetMinSeek method, IMSVidStreamBufferSink3.SetMinSeek, IMSVidStreamBufferSink3::SetMinSeek, IMSVidStreamBufferSink3SetMinSeek, SetMinSeek, SetMinSeek method [Microsoft TV Technologies], SetMinSeek method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_setminseek, segment/IMSVidStreamBufferSink3::SetMinSeek
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
-	IMSVidStreamBufferSink3.SetMinSeek
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSink3::SetMinSeek


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>SetMinSeek</b> method sets the minimum seek position equal to the current playback position, and retrieves the current position.


## -parameters




### -param pdwMin [out]

Receives the current position, in hundredths of seconds.


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




<a href="https://msdn.microsoft.com/5768936b-9c0a-4177-82da-cc6ebe62ea67">IMSVidStreamBufferSink3 Interface</a>
 

 

