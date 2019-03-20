---
UID: NF:segment.IMSVidPlayback.Run
title: IMSVidPlayback::Run (segment.h)
author: windows-sdk-content
description: The Run method runs the playback device.
old-location: mstv\imsvidplayback_run.htm
tech.root: mstv
ms.assetid: 58374819-82dd-4ffe-8cd7-ad51ea0d7207
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Run method, IMSVidPlayback.Run, IMSVidPlayback::Run, IMSVidPlaybackRun, Run, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_run, segment/IMSVidPlayback::Run
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
 - IMSVidPlayback.Run
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This method allows for direct control of the source. However, if the underlying source filter is controlled using the standard DirectShow <a href="https://msdn.microsoft.com/en-us/library/Dd390170(v=VS.85).aspx">IMediaControl</a> interface, this method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694586(v=VS.85).aspx">IMSVidPlayback Interface</a>
 

 

