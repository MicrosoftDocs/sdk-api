---
UID: NF:vidcap.IKsTopologyInfo.get_NumNodes
title: IKsTopologyInfo::get_NumNodes (vidcap.h)
description: The get_NumNodes method returns the number of nodes in the filter.
helpviewer_keywords: ["IKsTopologyInfo interface [DirectShow]","get_NumNodes method","IKsTopologyInfo.get_NumNodes","IKsTopologyInfo::get_NumNodes","IKsTopologyInfoget_NumNodes","dshow.ikstopologyinfo_get_numnodes","get_NumNodes","get_NumNodes method [DirectShow]","get_NumNodes method [DirectShow]","IKsTopologyInfo interface","vidcap/IKsTopologyInfo::get_NumNodes"]
old-location: dshow\ikstopologyinfo_get_numnodes.htm
tech.root: dshow
ms.assetid: fdba99d5-fd44-4d4f-8575-867d98bf3339
ms.date: 4/26/2023
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumNodes method, IKsTopologyInfo.get_NumNodes, IKsTopologyInfo::get_NumNodes, IKsTopologyInfoget_NumNodes, dshow.ikstopologyinfo_get_numnodes, get_NumNodes, get_NumNodes method [DirectShow], get_NumNodes method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumNodes
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
 - IKsTopologyInfo::get_NumNodes
 - vidcap/IKsTopologyInfo::get_NumNodes
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
 - IKsTopologyInfo.get_NumNodes
---

# IKsTopologyInfo::get_NumNodes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_NumNodes</code> method returns the number of nodes in the filter.

## -parameters

### -param pdwNumNodes [out]

Receives the number of nodes.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/ms785846(v=vs.85)">IKsTopologyInfo Interface</a>