---
UID: NF:vidcap.ISelector.get_SourceNodeId
title: ISelector::get_SourceNodeId (vidcap.h)
description: The get_SourceNodeId method returns the index of the active source node.
helpviewer_keywords: ["ISelector interface [DirectShow]","get_SourceNodeId method","ISelector.get_SourceNodeId","ISelector::get_SourceNodeId","ISelectorget_SourceNodeId","dshow.iselector_get_sourcenodeid","get_SourceNodeId","get_SourceNodeId method [DirectShow]","get_SourceNodeId method [DirectShow]","ISelector interface","vidcap/ISelector::get_SourceNodeId"]
old-location: dshow\iselector_get_sourcenodeid.htm
tech.root: dshow
ms.assetid: ae2b0e1a-1527-4634-b2f9-47c9519b55a6
ms.date: 4/26/2023
ms.keywords: ISelector interface [DirectShow],get_SourceNodeId method, ISelector.get_SourceNodeId, ISelector::get_SourceNodeId, ISelectorget_SourceNodeId, dshow.iselector_get_sourcenodeid, get_SourceNodeId, get_SourceNodeId method [DirectShow], get_SourceNodeId method [DirectShow],ISelector interface, vidcap/ISelector::get_SourceNodeId
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
 - ISelector::get_SourceNodeId
 - vidcap/ISelector::get_SourceNodeId
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
 - ISelector.get_SourceNodeId
---

# ISelector::get_SourceNodeId


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_SourceNodeId</code> method returns the index of the active source node.

## -parameters

### -param pdwPinId [out]

Receives the index of the source node that is currently active.

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



<a href="/windows/desktop/api/vidcap/nn-vidcap-iselector">ISelector Interface</a>