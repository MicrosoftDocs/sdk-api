---
UID: NF:vidcap.IKsTopologyInfo.CreateNodeInstance
title: IKsTopologyInfo::CreateNodeInstance (vidcap.h)
description: The CreateNodeInstance method creates a COM object that represents a node in the filter.
helpviewer_keywords: ["CreateNodeInstance","CreateNodeInstance method [DirectShow]","CreateNodeInstance method [DirectShow]","IKsTopologyInfo interface","IKsTopologyInfo interface [DirectShow]","CreateNodeInstance method","IKsTopologyInfo.CreateNodeInstance","IKsTopologyInfo::CreateNodeInstance","IKsTopologyInfoCreateNodeInstance","dshow.ikstopologyinfo_createnodeinstance","vidcap/IKsTopologyInfo::CreateNodeInstance"]
old-location: dshow\ikstopologyinfo_createnodeinstance.htm
tech.root: dshow
ms.assetid: f2c7ea1d-abd6-4179-b5b7-d89837ceecd7
ms.date: 4/26/2023
ms.keywords: CreateNodeInstance, CreateNodeInstance method [DirectShow], CreateNodeInstance method [DirectShow],IKsTopologyInfo interface, IKsTopologyInfo interface [DirectShow],CreateNodeInstance method, IKsTopologyInfo.CreateNodeInstance, IKsTopologyInfo::CreateNodeInstance, IKsTopologyInfoCreateNodeInstance, dshow.ikstopologyinfo_createnodeinstance, vidcap/IKsTopologyInfo::CreateNodeInstance
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
 - IKsTopologyInfo::CreateNodeInstance
 - vidcap/IKsTopologyInfo::CreateNodeInstance
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
 - IKsTopologyInfo.CreateNodeInstance
---

# IKsTopologyInfo::CreateNodeInstance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CreateNodeInstance</code> method creates a COM object that represents a node in the filter.

## -parameters

### -param dwNodeId [in]

Index of the node to create. To find the number of nodes, call the <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numnodes">IKsTopologyInfo::get_NumNodes</a> method.

### -param iid [in]

Interface identifier (IID) of the interface to return.

### -param ppvObject [out]

Receives a pointer to the requested interface on the node object. The caller must release the interface.

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

Node objects expose the <b>IKsControl</b> interface. You can use this interface to enumerate and access the node's property sets.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/ms785846(v=vs.85)">IKsTopologyInfo Interface</a>