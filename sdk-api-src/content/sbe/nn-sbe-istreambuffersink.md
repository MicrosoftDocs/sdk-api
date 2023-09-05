---
UID: NN:sbe.IStreamBufferSink
title: IStreamBufferSink (sbe.h)
description: The IStreamBufferSink interface is exposed by the Stream Buffer Sink filter. Use this interface to lock the filter before capture and to create new recordings.
helpviewer_keywords: ["IStreamBufferSink","IStreamBufferSink interface [Microsoft TV Technologies]","IStreamBufferSink interface [Microsoft TV Technologies]","described","IStreamBufferSinkInterface","mstv.istreambuffersink","sbe/IStreamBufferSink"]
old-location: mstv\istreambuffersink.htm
tech.root: mstv
ms.assetid: 4ae5a9e9-da51-4034-9a2c-22b57374deac
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink, IStreamBufferSink interface [Microsoft TV Technologies], IStreamBufferSink interface [Microsoft TV Technologies],described, IStreamBufferSinkInterface, mstv.istreambuffersink, sbe/IStreamBufferSink
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
 - IStreamBufferSink
 - sbe/IStreamBufferSink
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
 - IStreamBufferSink
---

# IStreamBufferSink interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferSink</b> interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter. Use this interface to lock the filter before capture and to create new recordings.

## -inheritance

The <b>IStreamBufferSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferSink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSink)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>



<a href="/previous-versions/windows/desktop/mstv/using-the-stream-buffer-engine">Using the Stream Buffer Engine</a>
