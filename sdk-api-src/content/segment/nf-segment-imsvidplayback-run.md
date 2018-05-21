---
UID: NF:segment.IMSVidPlayback.Run
title: IMSVidPlayback::Run
author: windows-driver-content
description: The Run method runs the playback device.
old-location: mstv\imsvidplayback_run.htm
old-project: mstv
ms.assetid: 58374819-82dd-4ffe-8cd7-ad51ea0d7207
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Run method, IMSVidPlayback.Run, IMSVidPlayback::Run, IMSVidPlaybackRun, Run, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_run, segment/IMSVidPlayback::Run
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMSVidPlayback.Run
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidPlayback::Run


## -description


The <b>Run</b> method runs the playback device.

Applications should call the <a href="https://msdn.microsoft.com/37ed6d7b-2e44-4bce-b476-8e8b28635346">IMSVidCtl::Run</a> method, rather than this method.


## -parameters






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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
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



This method allows for direct control of the source. However, if the underlying source filter is controlled using the standard DirectShow <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a> interface, this method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

