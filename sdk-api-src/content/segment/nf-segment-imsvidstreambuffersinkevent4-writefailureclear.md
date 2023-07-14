---
UID: NF:segment.IMSVidStreamBufferSinkEvent4.WriteFailureClear
title: IMSVidStreamBufferSinkEvent4::WriteFailureClear (segment.h)
description: The WriteFailureClear method is called when a write error from the Stream Buffer Sink filter has been cleared.
helpviewer_keywords: ["IMSVidStreamBufferSinkEvent4.WriteFailureClear","IMSVidStreamBufferSinkEvent4::WriteFailureClear","IMSVidstreamBufferSinkEvent4 interface [Microsoft TV Technologies]","WriteFailureClear method","IMSVidstreamBufferSinkEvent4::WriteFailureClear","WriteFailureClear","WriteFailureClear method [Microsoft TV Technologies]","WriteFailureClear method [Microsoft TV Technologies]","IMSVidstreamBufferSinkEvent4 interface","mstv.imsvidstreambuffersinkevent4_writefailureclear","segment/IMSVidstreamBufferSinkEvent4::WriteFailureClear"]
old-location: mstv\imsvidstreambuffersinkevent4_writefailureclear.htm
tech.root: mstv
ms.assetid: c5968d45-5fd2-460a-bbd8-38671bb98a14
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent4.WriteFailureClear, IMSVidStreamBufferSinkEvent4::WriteFailureClear, IMSVidstreamBufferSinkEvent4 interface [Microsoft TV Technologies],WriteFailureClear method, IMSVidstreamBufferSinkEvent4::WriteFailureClear, WriteFailureClear, WriteFailureClear method [Microsoft TV Technologies], WriteFailureClear method [Microsoft TV Technologies],IMSVidstreamBufferSinkEvent4 interface, mstv.imsvidstreambuffersinkevent4_writefailureclear, segment/IMSVidstreamBufferSinkEvent4::WriteFailureClear
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidStreamBufferSinkEvent4::WriteFailureClear
 - segment/IMSVidStreamBufferSinkEvent4::WriteFailureClear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidstreamBufferSinkEvent4.WriteFailureClear
---

# IMSVidStreamBufferSinkEvent4::WriteFailureClear


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>WriteFailureClear</b> method is called when a write error from the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink2-filter">Stream Buffer Sink</a> filter has been cleared.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent4">IMSVidStreamBufferSinkEvent4</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink2-filter">Stream Buffer Sink Filter</a>
