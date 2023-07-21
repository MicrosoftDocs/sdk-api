---
UID: NF:bdaiface.IBDA_Encoder.QueryCapabilities
title: IBDA_Encoder::QueryCapabilities (bdaiface.h)
description: Gets the number of encoding formats supported by the device.
helpviewer_keywords: ["IBDA_Encoder interface [Microsoft TV Technologies]","QueryCapabilities method","IBDA_Encoder.QueryCapabilities","IBDA_Encoder::QueryCapabilities","QueryCapabilities","QueryCapabilities method [Microsoft TV Technologies]","QueryCapabilities method [Microsoft TV Technologies]","IBDA_Encoder interface","bdaiface/IBDA_Encoder::QueryCapabilities","mstv.ibda_encoder_querycapabilities"]
old-location: mstv\ibda_encoder_querycapabilities.htm
tech.root: mstv
ms.assetid: 038f9360-0515-4655-9397-cd1bfb6c3d21
ms.date: 12/05/2018
ms.keywords: IBDA_Encoder interface [Microsoft TV Technologies],QueryCapabilities method, IBDA_Encoder.QueryCapabilities, IBDA_Encoder::QueryCapabilities, QueryCapabilities, QueryCapabilities method [Microsoft TV Technologies], QueryCapabilities method [Microsoft TV Technologies],IBDA_Encoder interface, bdaiface/IBDA_Encoder::QueryCapabilities, mstv.ibda_encoder_querycapabilities
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IBDA_Encoder::QueryCapabilities
 - bdaiface/IBDA_Encoder::QueryCapabilities
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
 - IBDA_Encoder.QueryCapabilities
---

# IBDA_Encoder::QueryCapabilities


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of encoding formats supported by the device.

## -parameters

### -param NumAudioFmts [out]

Receives the number of audio formats.

### -param NumVideoFmts [out]

Receives the number of video formats.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_encoder">IBDA_Encoder</a>