---
UID: NF:vidcap.IKsNodeControl.put_NodeId
title: IKsNodeControl::put_NodeId (vidcap.h)
description: Sets the node identifier for the extension unit.
helpviewer_keywords: ["IKsNodeControl interface [DirectShow]","put_NodeId method","IKsNodeControl.put_NodeId","IKsNodeControl::put_NodeId","IKsNodeControlput_NodeId","dshow.iksnodecontrol_put_nodeid","put_NodeId","put_NodeId method [DirectShow]","put_NodeId method [DirectShow]","IKsNodeControl interface","vidcap/IKsNodeControl::put_NodeId"]
old-location: dshow\iksnodecontrol_put_nodeid.htm
tech.root: dshow
ms.assetid: 3f18085c-5a5c-4bc3-84e2-50fbf2319072
ms.date: 4/26/2023
ms.keywords: IKsNodeControl interface [DirectShow],put_NodeId method, IKsNodeControl.put_NodeId, IKsNodeControl::put_NodeId, IKsNodeControlput_NodeId, dshow.iksnodecontrol_put_nodeid, put_NodeId, put_NodeId method [DirectShow], put_NodeId method [DirectShow],IKsNodeControl interface, vidcap/IKsNodeControl::put_NodeId
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
 - IKsNodeControl::put_NodeId
 - vidcap/IKsNodeControl::put_NodeId
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
 - IKsNodeControl.put_NodeId
---

# IKsNodeControl::put_NodeId


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Sets the node identifier for the extension unit.

## -parameters

### -param dwNodeId [in]

Node identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-iksnodecontrol">IKsNodeControl Interface</a>