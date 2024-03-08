---
UID: NN:tuner.IMPEG2Component
title: IMPEG2Component (tuner.h)
description: The IMPEG2Component interface contains methods for getting and setting properties that describe an MPEG2 elementary stream.
helpviewer_keywords: ["IMPEG2Component","IMPEG2Component interface [Microsoft TV Technologies]","IMPEG2Component interface [Microsoft TV Technologies]","described","IMPEG2ComponentInterface","mstv.impeg2component","tuner/IMPEG2Component"]
old-location: mstv\impeg2component.htm
tech.root: mstv
ms.assetid: 63d1ae17-8e38-457e-98d7-e81e7576f1c1
ms.date: 12/05/2018
ms.keywords: IMPEG2Component, IMPEG2Component interface [Microsoft TV Technologies], IMPEG2Component interface [Microsoft TV Technologies],described, IMPEG2ComponentInterface, mstv.impeg2component, tuner/IMPEG2Component
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IMPEG2Component
 - tuner/IMPEG2Component
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IMPEG2Component
---

# IMPEG2Component interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMPEG2Component</b> interface contains methods for getting and setting properties that describe an MPEG2 elementary stream. These properties are set by the TIF or Guide Store loader based on data in the transport stream tables. After the tune request is retrieved from the Guide Store and submitted either to the Video Control or directly to the Network Provider, these properties are used by the Network Provider and MPEG-2 Demultiplexer to acquire the specified substream and pass it to the downstream filters.

## -inheritance

The <b>IMPEG2Component</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a>. <b>IMPEG2Component</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2Component)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
