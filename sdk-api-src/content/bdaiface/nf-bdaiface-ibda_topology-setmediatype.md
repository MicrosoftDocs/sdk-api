---
UID: NF:bdaiface.IBDA_Topology.SetMediaType
title: IBDA_Topology::SetMediaType (bdaiface.h)
description: The SetMediaType method sets the media type for a pin on a BDA device filter.
helpviewer_keywords: ["IBDA_Topology interface [Microsoft TV Technologies]","SetMediaType method","IBDA_Topology.SetMediaType","IBDA_Topology::SetMediaType","IBDA_TopologySetMediaType","SetMediaType","SetMediaType method [Microsoft TV Technologies]","SetMediaType method [Microsoft TV Technologies]","IBDA_Topology interface","bdaiface/IBDA_Topology::SetMediaType","mstv.ibda_topology_setmediatype"]
old-location: mstv\ibda_topology_setmediatype.htm
tech.root: mstv
ms.assetid: 69cedd00-3a32-4fb9-91af-2980c314324f
ms.date: 12/05/2018
ms.keywords: IBDA_Topology interface [Microsoft TV Technologies],SetMediaType method, IBDA_Topology.SetMediaType, IBDA_Topology::SetMediaType, IBDA_TopologySetMediaType, SetMediaType, SetMediaType method [Microsoft TV Technologies], SetMediaType method [Microsoft TV Technologies],IBDA_Topology interface, bdaiface/IBDA_Topology::SetMediaType, mstv.ibda_topology_setmediatype
req.header: bdaiface.h
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
 - IBDA_Topology::SetMediaType
 - bdaiface/IBDA_Topology::SetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Topology.SetMediaType
---

# IBDA_Topology::SetMediaType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetMediaType</b> method sets the media type for a pin on a BDA device filter.

## -parameters

### -param ulPinId [in]

The identifier of the pin on which to set the media type.

### -param pMediaType [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that contains the media type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>