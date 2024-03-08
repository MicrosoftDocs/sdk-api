---
UID: NN:sbe.IStreamBufferDataCounters
title: IStreamBufferDataCounters (sbe.h)
description: The IStreamBufferDataCounters interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the Stream Buffer Sink filter and the Stream Buffer Source filter.
helpviewer_keywords: ["IStreamBufferDataCounters","IStreamBufferDataCounters interface [Microsoft TV Technologies]","IStreamBufferDataCounters interface [Microsoft TV Technologies]","described","IStreamBufferDataCountersInterface","mstv.istreambufferdatacounters","sbe/IStreamBufferDataCounters"]
old-location: mstv\istreambufferdatacounters.htm
tech.root: mstv
ms.assetid: d9394d04-ba6b-4946-b33a-9c53070238f7
ms.date: 12/05/2018
ms.keywords: IStreamBufferDataCounters, IStreamBufferDataCounters interface [Microsoft TV Technologies], IStreamBufferDataCounters interface [Microsoft TV Technologies],described, IStreamBufferDataCountersInterface, mstv.istreambufferdatacounters, sbe/IStreamBufferDataCounters
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IStreamBufferDataCounters
 - sbe/IStreamBufferDataCounters
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
 - IStreamBufferDataCounters
---

# IStreamBufferDataCounters interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferDataCounters</b> interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter and the Stream Buffer Source filter.

## -inheritance

The <b>IStreamBufferDataCounters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferDataCounters</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferDataCounters)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
