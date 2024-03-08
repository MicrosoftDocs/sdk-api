---
UID: NN:mpeg2data.IMpeg2Stream
title: IMpeg2Stream (mpeg2data.h)
description: The IMpeg2Stream interface represents a stream of MPEG-2 data. The IMpeg2Data::GetStreamOfSections method returns a pointer to this interface.
helpviewer_keywords: ["IMpeg2Stream","IMpeg2Stream interface [Microsoft TV Technologies]","IMpeg2Stream interface [Microsoft TV Technologies]","described","IMpeg2StreamInterface","mpeg2data/IMpeg2Stream","mstv.impeg2stream"]
old-location: mstv\impeg2stream.htm
tech.root: mstv
ms.assetid: 189c921a-ec49-48dc-8c60-3d3ec2a648ca
ms.date: 12/05/2018
ms.keywords: IMpeg2Stream, IMpeg2Stream interface [Microsoft TV Technologies], IMpeg2Stream interface [Microsoft TV Technologies],described, IMpeg2StreamInterface, mpeg2data/IMpeg2Stream, mstv.impeg2stream
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMpeg2Stream
 - mpeg2data/IMpeg2Stream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2Stream
---

# IMpeg2Stream interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMpeg2Stream</b> interface represents a stream of MPEG-2 data. The <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getstreamofsections">IMpeg2Data::GetStreamOfSections</a> method returns a pointer to this interface.

## -inheritance

The <b>IMpeg2Stream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2Stream</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2Stream)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
