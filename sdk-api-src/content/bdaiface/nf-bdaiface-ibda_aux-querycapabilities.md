---
UID: NF:bdaiface.IBDA_AUX.QueryCapabilities
title: IBDA_AUX::QueryCapabilities (bdaiface.h)
description: Gets the number of auxiliary connectors on the device.
helpviewer_keywords: ["IBDA_AUX interface [Microsoft TV Technologies]","QueryCapabilities method","IBDA_AUX.QueryCapabilities","IBDA_AUX::QueryCapabilities","QueryCapabilities","QueryCapabilities method [Microsoft TV Technologies]","QueryCapabilities method [Microsoft TV Technologies]","IBDA_AUX interface","bdaiface/IBDA_AUX::QueryCapabilities","mstv.ibda_aux_querycapabilities"]
old-location: mstv\ibda_aux_querycapabilities.htm
tech.root: mstv
ms.assetid: 7bb80ae2-050e-4fe6-9dd4-9cc6b2bcdd3c
ms.date: 12/05/2018
ms.keywords: IBDA_AUX interface [Microsoft TV Technologies],QueryCapabilities method, IBDA_AUX.QueryCapabilities, IBDA_AUX::QueryCapabilities, QueryCapabilities, QueryCapabilities method [Microsoft TV Technologies], QueryCapabilities method [Microsoft TV Technologies],IBDA_AUX interface, bdaiface/IBDA_AUX::QueryCapabilities, mstv.ibda_aux_querycapabilities
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_AUX::QueryCapabilities
 - bdaiface/IBDA_AUX::QueryCapabilities
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
 - IBDA_AUX.QueryCapabilities
---

# IBDA_AUX::QueryCapabilities


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of auxiliary connectors on the device.

## -parameters

### -param pdwNumAuxInputsBSTR [out]

Receives the number of auxiliary connectors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_aux">IBDA_AUX</a>