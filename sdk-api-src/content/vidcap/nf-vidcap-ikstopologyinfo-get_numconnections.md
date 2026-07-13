---
UID: NF:vidcap.IKsTopologyInfo.get_NumConnections
title: IKsTopologyInfo::get_NumConnections (vidcap.h)
description: The get_NumConnections method returns the number of node connections within the filter.
helpviewer_keywords: ["IKsTopologyInfo interface [DirectShow]","get_NumConnections method","IKsTopologyInfo.get_NumConnections","IKsTopologyInfo::get_NumConnections","IKsTopologyInfoget_NumConnections","dshow.ikstopologyinfo_get_numconnections","get_NumConnections","get_NumConnections method [DirectShow]","get_NumConnections method [DirectShow]","IKsTopologyInfo interface","vidcap/IKsTopologyInfo::get_NumConnections"]
old-location: dshow\ikstopologyinfo_get_numconnections.htm
tech.root: dshow
ms.assetid: 55f52b02-2768-4c59-9275-96e238ccf3f0
ms.date: 4/26/2023
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumConnections method, IKsTopologyInfo.get_NumConnections, IKsTopologyInfo::get_NumConnections, IKsTopologyInfoget_NumConnections, dshow.ikstopologyinfo_get_numconnections, get_NumConnections, get_NumConnections method [DirectShow], get_NumConnections method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumConnections
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IKsTopologyInfo::get_NumConnections
 - vidcap/IKsTopologyInfo::get_NumConnections
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NumConnections
---

# IKsTopologyInfo::get_NumConnections


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_NumConnections</code> method returns the number of node connections within the filter.

## -parameters

### -param pdwNumConnections [out]

Receives the number of connections.

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

## -remarks

To get information about the connections, call the <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo">IKsTopologyInfo::get_ConnectionInfo</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/ms785846(v=vs.85)">IKsTopologyInfo Interface</a>