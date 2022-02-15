---
UID: NN:vidcap.ICameraControl
title: ICameraControl (vidcap.h)
description: The ICameraControl interface controls the camera settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
helpviewer_keywords: ["ICameraControl","ICameraControl interface [DirectShow]","ICameraControl interface [DirectShow]","described","ICameraControlInterface","dshow.icameracontrol","vidcap/ICameraControl"]
old-location: dshow\icameracontrol.htm
tech.root: dshow
ms.assetid: 7046f96d-a613-4056-84dd-be022efdda4f
ms.date: 12/05/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], ICameraControl interface [DirectShow],described, ICameraControlInterface, dshow.icameracontrol, vidcap/ICameraControl
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICameraControl
 - vidcap/ICameraControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl
---

# ICameraControl interface


## -description

The <code>ICameraControl</code> interface controls the camera settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="/windows/previous-versions/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo</a> interface. For each node, call <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodetype">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>ICameraControl</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_CAMERA_TERMINAL. Get the interface pointer by calling <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_ICameraControl.

This interface corresponds to the PROPSETID_VIDCAP_CAMERACONTROL property set, which is documented in the Windows DDK.

## -inheritance

The <b>ICameraControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICameraControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

