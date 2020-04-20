---
UID: NF:tuner.IMPEG2ComponentType.get_StreamType
title: IMPEG2ComponentType::get_StreamType (tuner.h)
description: The get_StreamType method retrieves the stream type.helpviewer_keywords: ["IMPEG2ComponentType interface [Microsoft TV Technologies]","get_StreamType method","IMPEG2ComponentType.get_StreamType","IMPEG2ComponentType::get_StreamType","IMPEG2ComponentTypeget_StreamType","get_StreamType","get_StreamType method [Microsoft TV Technologies]","get_StreamType method [Microsoft TV Technologies]","IMPEG2ComponentType interface","mstv.impeg2componenttype_get_streamtype","tuner/IMPEG2ComponentType::get_StreamType"]
old-location: mstv\impeg2componenttype_get_streamtype.htm
tech.root: mstv
ms.assetid: c3aa2a63-aa02-41c3-bbdf-f155346eea0a
ms.date: 12/05/2018
ms.keywords: IMPEG2ComponentType interface [Microsoft TV Technologies],get_StreamType method, IMPEG2ComponentType.get_StreamType, IMPEG2ComponentType::get_StreamType, IMPEG2ComponentTypeget_StreamType, get_StreamType, get_StreamType method [Microsoft TV Technologies], get_StreamType method [Microsoft TV Technologies],IMPEG2ComponentType interface, mstv.impeg2componenttype_get_streamtype, tuner/IMPEG2ComponentType::get_StreamType
f1_keywords:
- tuner/IMPEG2ComponentType.get_StreamType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IMPEG2ComponentType.get_StreamType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2ComponentType::get_StreamType


## -description



The <b>get_StreamType</b> method retrieves the stream type.




## -parameters




### -param MP2StreamType [out]

Pointer to a variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/mpeg2streamtype">MPEG2StreamType</a> that receives the stream type value.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType Interface</a>
 

 

