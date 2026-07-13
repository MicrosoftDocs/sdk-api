---
UID: NF:vidcap.IKsTopologyInfo.get_ConnectionInfo
title: IKsTopologyInfo::get_ConnectionInfo (vidcap.h)
description: The get_ConnectionInfo method returns information about one node connection in the filter.
helpviewer_keywords: ["IKsTopologyInfo interface [DirectShow]","get_ConnectionInfo method","IKsTopologyInfo.get_ConnectionInfo","IKsTopologyInfo::get_ConnectionInfo","IKsTopologyInfoget_ConnectionInfo","dshow.ikstopologyinfo_get_connectioninfo","get_ConnectionInfo","get_ConnectionInfo method [DirectShow]","get_ConnectionInfo method [DirectShow]","IKsTopologyInfo interface","vidcap/IKsTopologyInfo::get_ConnectionInfo"]
old-location: dshow\ikstopologyinfo_get_connectioninfo.htm
tech.root: dshow
ms.assetid: ef062e0f-0866-48ca-bd27-26000cd4983a
ms.date: 4/26/2023
ms.keywords: IKsTopologyInfo interface [DirectShow],get_ConnectionInfo method, IKsTopologyInfo.get_ConnectionInfo, IKsTopologyInfo::get_ConnectionInfo, IKsTopologyInfoget_ConnectionInfo, dshow.ikstopologyinfo_get_connectioninfo, get_ConnectionInfo, get_ConnectionInfo method [DirectShow], get_ConnectionInfo method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_ConnectionInfo
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
 - IKsTopologyInfo::get_ConnectionInfo
 - vidcap/IKsTopologyInfo::get_ConnectionInfo
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
 - IKsTopologyInfo.get_ConnectionInfo
---

# IKsTopologyInfo::get_ConnectionInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ConnectionInfo</code> method returns information about one node connection in the filter.

## -parameters

### -param dwIndex [in]

Index of the connection. To find the number of connections, call the <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numconnections">IKsTopologyInfo::get_NumConnections</a> method.

### -param pConnectionInfo [out]

Pointer to a <a href="/windows/desktop/DirectShow/kstopology-connection">KSTOPOLOGY_CONNECTION</a> structure allocated by the caller. The method fills in this structure with the connection information.

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