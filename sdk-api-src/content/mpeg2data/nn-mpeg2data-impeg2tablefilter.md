---
UID: NN:mpeg2data.IMpeg2TableFilter
title: IMpeg2TableFilter (mpeg2data.h)
description: The IMpeg2TableFilter interface controls which tables are parsed by the MPEG-2 Sections and Tables filter. The BDA MPEG-2 Transport Information filter exposes this interface on its output pins.
helpviewer_keywords: ["IMpeg2TableFilter","IMpeg2TableFilter interface [Microsoft TV Technologies]","IMpeg2TableFilter interface [Microsoft TV Technologies]","described","IMpeg2TableFilterInterface","mpeg2data/IMpeg2TableFilter","mstv.impeg2tablefilter"]
old-location: mstv\impeg2tablefilter.htm
tech.root: mstv
ms.assetid: 9467352d-44a5-41eb-b426-28df83a6d423
ms.date: 12/05/2018
ms.keywords: IMpeg2TableFilter, IMpeg2TableFilter interface [Microsoft TV Technologies], IMpeg2TableFilter interface [Microsoft TV Technologies],described, IMpeg2TableFilterInterface, mpeg2data/IMpeg2TableFilter, mstv.impeg2tablefilter
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
 - IMpeg2TableFilter
 - mpeg2data/IMpeg2TableFilter
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
 - IMpeg2TableFilter
---

# IMpeg2TableFilter interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMpeg2TableFilter</b> interface controls which tables are parsed by the <a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter. The <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information</a> filter exposes this interface on its output pins.

## -inheritance

The <b>IMpeg2TableFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2TableFilter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2TableFilter)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a>



<a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables Filter</a>
