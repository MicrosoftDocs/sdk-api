---
UID: NF:segment.IMSVidStreamBufferSink3.SetMinSeek
title: IMSVidStreamBufferSink3::SetMinSeek (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSink3 interface [Microsoft TV Technologies]","SetMinSeek method","IMSVidStreamBufferSink3.SetMinSeek","IMSVidStreamBufferSink3::SetMinSeek","IMSVidStreamBufferSink3SetMinSeek","SetMinSeek","SetMinSeek method [Microsoft TV Technologies]","SetMinSeek method [Microsoft TV Technologies]","IMSVidStreamBufferSink3 interface","mstv.imsvidstreambuffersink3_setminseek","segment/IMSVidStreamBufferSink3::SetMinSeek"]
old-location: mstv\imsvidstreambuffersink3_setminseek.htm
tech.root: mstv
ms.assetid: 2f7a7323-c9da-47f9-95e2-dd13fc023373
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],SetMinSeek method, IMSVidStreamBufferSink3.SetMinSeek, IMSVidStreamBufferSink3::SetMinSeek, IMSVidStreamBufferSink3SetMinSeek, SetMinSeek, SetMinSeek method [Microsoft TV Technologies], SetMinSeek method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_setminseek, segment/IMSVidStreamBufferSink3::SetMinSeek
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSink3::SetMinSeek
 - segment/IMSVidStreamBufferSink3::SetMinSeek
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
 - IMSVidStreamBufferSink3.SetMinSeek
---

# IMSVidStreamBufferSink3::SetMinSeek


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersink3">IMSVidStreamBufferSink3 Interface</a>