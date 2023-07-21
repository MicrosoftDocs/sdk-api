---
UID: NN:sbe.IStreamBufferMediaSeeking2
title: IStreamBufferMediaSeeking2 (sbe.h)
description: The IStreamBufferMediaSeeking2 interface is exposed by the Stream Buffer Source filter. It provides a method to control the frame rate during fast-forward play (&#0034;trick mode&#0034;).
helpviewer_keywords: ["IStreamBufferMediaSeeking2","IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies]","IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies]","described","IStreamBufferMediaSeeking2Interface","mstv.istreambuffermediaseeking2","sbe/IStreamBufferMediaSeeking2"]
old-location: mstv\istreambuffermediaseeking2.htm
tech.root: mstv
ms.assetid: 3029868e-0b27-4ce9-90b2-22d8e1961a1f
ms.date: 12/05/2018
ms.keywords: IStreamBufferMediaSeeking2, IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies], IStreamBufferMediaSeeking2 interface [Microsoft TV Technologies],described, IStreamBufferMediaSeeking2Interface, mstv.istreambuffermediaseeking2, sbe/IStreamBufferMediaSeeking2
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
 - IStreamBufferMediaSeeking2
 - sbe/IStreamBufferMediaSeeking2
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
 - IStreamBufferMediaSeeking2
---

# IStreamBufferMediaSeeking2 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferMediaSeeking2</b> interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter. It provides a method to control the frame rate during fast-forward play ("trick mode").

## -inheritance

The <b>IStreamBufferMediaSeeking2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffermediaseeking">IStreamBufferMediaSeeking</a>. <b>IStreamBufferMediaSeeking2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferMediaSeeking2)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffermediaseeking">IStreamBufferMediaSeeking</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
