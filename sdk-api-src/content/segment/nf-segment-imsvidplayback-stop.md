---
UID: NF:segment.IMSVidPlayback.Stop
title: IMSVidPlayback::Stop
author: windows-sdk-content
description: The Stop method stops the playback device.
old-location: mstv\imsvidplayback_stop.htm
tech.root: mstv
ms.assetid: 20262521-bb9c-4e37-b89c-8c439df50ed4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Stop method, IMSVidPlayback.Stop, IMSVidPlayback::Stop, IMSVidPlaybackStop, Stop, Stop method [Microsoft TV Technologies], Stop method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_stop, segment/IMSVidPlayback::Stop
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



This method allows for direct control of the source. However, if the underlying source filter is controlled using the standard DirectShow <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a> interface, this method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 

