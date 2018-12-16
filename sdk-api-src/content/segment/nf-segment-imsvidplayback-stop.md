---
UID: NF:segment.IMSVidPlayback.Stop
title: IMSVidPlayback::Stop
author: windows-sdk-content
description: The Stop method stops the playback device.
old-location: mstv\imsvidplayback_stop.htm
tech.root: mstv
ms.assetid: 20262521-bb9c-4e37-b89c-8c439df50ed4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Stop method, IMSVidPlayback.Stop, IMSVidPlayback::Stop, IMSVidPlaybackStop, Stop, Stop method [Microsoft TV Technologies], Stop method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_stop, segment/IMSVidPlayback::Stop
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
 - IMSVidPlayback.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidPlayback::Stop


## -description


The <b>Stop</b> method stops the playback device.

Applications should call the <a href="https://msdn.microsoft.com/8ca43663-3726-4147-8774-2f1eecef9142">IMSVidCtl::Stop</a> method, rather than this method.


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
 

 

