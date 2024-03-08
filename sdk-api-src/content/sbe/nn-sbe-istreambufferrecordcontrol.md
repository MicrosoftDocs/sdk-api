---
UID: NN:sbe.IStreamBufferRecordControl
title: IStreamBufferRecordControl (sbe.h)
description: The IStreamBufferRecordControl interface is used to control stream buffer Recording objects.Use the IStreamBufferSink::CreateRecorder method on the Stream Buffer Sink filter to create new Recording objects.
helpviewer_keywords: ["IStreamBufferRecordControl","IStreamBufferRecordControl interface [Microsoft TV Technologies]","IStreamBufferRecordControl interface [Microsoft TV Technologies]","described","IStreamBufferRecordControlInterface","mstv.istreambufferrecordcontrol","sbe/IStreamBufferRecordControl"]
old-location: mstv\istreambufferrecordcontrol.htm
tech.root: mstv
ms.assetid: f196638e-ccbb-4768-96c1-8e1d00361831
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordControl, IStreamBufferRecordControl interface [Microsoft TV Technologies], IStreamBufferRecordControl interface [Microsoft TV Technologies],described, IStreamBufferRecordControlInterface, mstv.istreambufferrecordcontrol, sbe/IStreamBufferRecordControl
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
 - IStreamBufferRecordControl
 - sbe/IStreamBufferRecordControl
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
 - IStreamBufferRecordControl
---

# IStreamBufferRecordControl interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferRecordControl</b> interface is used to control stream buffer <a href="/previous-versions/windows/desktop/mstv/recording-object">Recording</a> objects.

Use the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-createrecorder">IStreamBufferSink::CreateRecorder</a> method on the Stream Buffer Sink filter to create new Recording objects. After making a recording, stop the <b>Recording</b> object and release it before releasing the Stream Buffer Sink filter.

## -inheritance

The <b>IStreamBufferRecordControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecordControl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordControl)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/creating-stream-buffer-recordings">Creating Stream Buffer Recordings</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
