---
UID: NF:segment.IMSVidStreamBufferSink.NameSetLock
title: IMSVidStreamBufferSink::NameSetLock (segment.h)
description: The NameSetLock method locks the stream buffer profile.
helpviewer_keywords: ["IMSVidStreamBufferSink interface [Microsoft TV Technologies]","NameSetLock method","IMSVidStreamBufferSink.NameSetLock","IMSVidStreamBufferSink::NameSetLock","IMSVidStreamBufferSinkNameSetLock","NameSetLock","NameSetLock method [Microsoft TV Technologies]","NameSetLock method [Microsoft TV Technologies]","IMSVidStreamBufferSink interface","mstv.imsvidstreambuffersink_namesetlock","segment/IMSVidStreamBufferSink::NameSetLock"]
old-location: mstv\imsvidstreambuffersink_namesetlock.htm
tech.root: mstv
ms.assetid: 0195d515-4018-4a96-9af9-566fcdeffaf7
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],NameSetLock method, IMSVidStreamBufferSink.NameSetLock, IMSVidStreamBufferSink::NameSetLock, IMSVidStreamBufferSinkNameSetLock, NameSetLock, NameSetLock method [Microsoft TV Technologies], NameSetLock method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_namesetlock, segment/IMSVidStreamBufferSink::NameSetLock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSink::NameSetLock
 - segment/IMSVidStreamBufferSink::NameSetLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSink.NameSetLock
---

# IMSVidStreamBufferSink::NameSetLock


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>NameSetLock</b> method locks the stream buffer profile.



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

<a href="/previous-versions/windows/desktop/mstv/buffering-in-the-stream-buffer-engine">Buffering in the Stream Buffer Engine</a>



<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersink">IMSVidStreamBufferSink Interface</a>
