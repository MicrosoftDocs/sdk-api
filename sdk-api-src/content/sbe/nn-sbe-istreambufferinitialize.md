---
UID: NN:sbe.IStreamBufferInitialize
title: IStreamBufferInitialize (sbe.h)
description: The IStreamBufferInitialize interface is used to configure the stream buffer filters. The Stream Buffer Source filter, Stream Buffer Sink filter, and StreamBufferConfig object all expose this interface.
helpviewer_keywords: ["IStreamBufferInitialize","IStreamBufferInitialize interface [Microsoft TV Technologies]","IStreamBufferInitialize interface [Microsoft TV Technologies]","described","IStreamBufferInitializeInterface","mstv.istreambufferinitialize","sbe/IStreamBufferInitialize"]
old-location: mstv\istreambufferinitialize.htm
tech.root: mstv
ms.assetid: 357b2979-78de-4a99-bf52-4117af7dfaad
ms.date: 12/05/2018
ms.keywords: IStreamBufferInitialize, IStreamBufferInitialize interface [Microsoft TV Technologies], IStreamBufferInitialize interface [Microsoft TV Technologies],described, IStreamBufferInitializeInterface, mstv.istreambufferinitialize, sbe/IStreamBufferInitialize
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IStreamBufferInitialize
 - sbe/IStreamBufferInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferInitialize
---

# IStreamBufferInitialize interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferInitialize</b> interface is used to configure the stream buffer filters. The <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter, <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter, and <a href="/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object all expose this interface.

## -inheritance

The <b>IStreamBufferInitialize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferInitialize</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferInitialize)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
