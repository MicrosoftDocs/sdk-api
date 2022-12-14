---
UID: NN:vidcap.IVideoProcAmp
title: IVideoProcAmp (vidcap.h)
description: The IVideoProcAmp interface controls the image adjustment (ProcAmp) settings on a capture device.This interface may be exposed by one or more nodes in a capture filter.
helpviewer_keywords: ["IVideoProcAmp","IVideoProcAmp interface [DirectShow]","IVideoProcAmp interface [DirectShow]","described","IVideoProcAmpInterface","dshow.ivideoprocamp","vidcap/IVideoProcAmp"]
old-location: dshow\ivideoprocamp.htm
tech.root: dshow
ms.assetid: efaef34a-688a-4c7d-b8ee-e0f52468e355
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp, IVideoProcAmp interface [DirectShow], IVideoProcAmp interface [DirectShow],described, IVideoProcAmpInterface, dshow.ivideoprocamp, vidcap/IVideoProcAmp
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
 - IVideoProcAmp
 - vidcap/IVideoProcAmp
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
 - IVideoProcAmp
---

# IVideoProcAmp interface


## -description

The <code>IVideoProcAmp</code> interface controls the image adjustment (ProcAmp) settings on a capture device.

This interface may be exposed by one or more nodes in a capture filter. It is not exposed at the level of the filter itself. To enumerate the nodes, query the filter for the <a href="/windows/previous-versions/windows/desktop/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo</a> interface. For each node, call <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_nodetype">IKsTopologyInfo::get_NodeType</a> to get the node type. The <code>IVideoProcAmp</code> interface is exposed by nodes of type KSNODETYPE_VIDEO_PROCESSING. Get the interface pointer by calling <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-createnodeinstance">IKsTopologyInfo::CreateNodeInstance</a> with the value IID_IVideoProcAmp.

This interface corresponds to the PROPSETID_VIDCAP_VIDEOPROCAMP property set, which is documented in the Windows DDK.

## -inheritance

The <b>IVideoProcAmp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVideoProcAmp</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

