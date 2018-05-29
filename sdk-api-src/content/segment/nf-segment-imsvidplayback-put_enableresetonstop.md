---
UID: NF:segment.IMSVidPlayback.put_EnableResetOnStop
title: IMSVidPlayback::put_EnableResetOnStop
author: windows-sdk-content
description: The put_EnableResetOnStop method indicates how playback will resume if the graph is rebuilt.
old-location: mstv\imsvidplayback_put_enableresetonstop.htm
old-project: mstv
ms.assetid: f2b4285c-3cf8-40dc-87eb-57419ef7343e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],put_EnableResetOnStop method, IMSVidPlayback.put_EnableResetOnStop, IMSVidPlayback::put_EnableResetOnStop, IMSVidPlaybackput_EnableResetOnStop, mstv.imsvidplayback_put_enableresetonstop, put_EnableResetOnStop, put_EnableResetOnStop method [Microsoft TV Technologies], put_EnableResetOnStop method [Microsoft TV Technologies],IMSVidPlayback interface, segment/IMSVidPlayback::put_EnableResetOnStop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
-	IMSVidPlayback.put_EnableResetOnStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

