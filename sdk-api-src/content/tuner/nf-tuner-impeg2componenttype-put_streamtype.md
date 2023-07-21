---
UID: NF:tuner.IMPEG2ComponentType.put_StreamType
title: IMPEG2ComponentType::put_StreamType (tuner.h)
description: The put_StreamType method sets the MPEG2 stream type.
helpviewer_keywords: ["IMPEG2ComponentType interface [Microsoft TV Technologies]","put_StreamType method","IMPEG2ComponentType.put_StreamType","IMPEG2ComponentType::put_StreamType","IMPEG2ComponentTypeput_StreamType","mstv.impeg2componenttype_put_streamtype","put_StreamType","put_StreamType method [Microsoft TV Technologies]","put_StreamType method [Microsoft TV Technologies]","IMPEG2ComponentType interface","tuner/IMPEG2ComponentType::put_StreamType"]
old-location: mstv\impeg2componenttype_put_streamtype.htm
tech.root: mstv
ms.assetid: 5dbfacf3-87e2-48d4-add9-6da68c56af82
ms.date: 12/05/2018
ms.keywords: IMPEG2ComponentType interface [Microsoft TV Technologies],put_StreamType method, IMPEG2ComponentType.put_StreamType, IMPEG2ComponentType::put_StreamType, IMPEG2ComponentTypeput_StreamType, mstv.impeg2componenttype_put_streamtype, put_StreamType, put_StreamType method [Microsoft TV Technologies], put_StreamType method [Microsoft TV Technologies],IMPEG2ComponentType interface, tuner/IMPEG2ComponentType::put_StreamType
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IMPEG2ComponentType::put_StreamType
 - tuner/IMPEG2ComponentType::put_StreamType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IMPEG2ComponentType.put_StreamType
---

# IMPEG2ComponentType::put_StreamType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_StreamType</b> method sets the MPEG2 stream type.

## -parameters

### -param MP2StreamType [in]

Variable of type <a href="/previous-versions/windows/desktop/mstv/mpeg2streamtype">MPEG2StreamType</a> that specifies the stream type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType Interface</a>