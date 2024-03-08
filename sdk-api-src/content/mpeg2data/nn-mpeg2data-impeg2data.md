---
UID: NN:mpeg2data.IMpeg2Data
title: IMpeg2Data (mpeg2data.h)
description: IMpeg2Data is no longer available for use as of Windows 7.
helpviewer_keywords: ["IMpeg2Data","IMpeg2Data interface [Microsoft TV Technologies]","IMpeg2Data interface [Microsoft TV Technologies]","described","IMpeg2DataInterface","mpeg2data/IMpeg2Data","mstv.impeg2data"]
old-location: mstv\impeg2data.htm
tech.root: mstv
ms.assetid: 82af47a2-cac4-4d4f-ba20-d4f6b5485a65
ms.date: 12/05/2018
ms.keywords: IMpeg2Data, IMpeg2Data interface [Microsoft TV Technologies], IMpeg2Data interface [Microsoft TV Technologies],described, IMpeg2DataInterface, mpeg2data/IMpeg2Data, mstv.impeg2data
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
 - IMpeg2Data
 - mpeg2data/IMpeg2Data
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
 - IMpeg2Data
---

# IMpeg2Data interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>IMpeg2Data</b> is no longer available for use as of Windows 7. Instead, use the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

The <b>IMpeg2Data</b> interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter. It enables the client to retrieve unparsed sections or tables from an MPEG-2 transport stream.

## -inheritance

The <b>IMpeg2Data</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2Data</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2Data)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/previous-versions/windows/desktop/mstv/getting-mpeg2-psi-tables">Getting MPEG-2 PSI Tables</a>
