---
UID: NF:tuner.IComponentType.get_MediaFormatType
title: IComponentType::get_MediaFormatType (tuner.h)
description: The get_MediaFormatType method retrieves the DirectShow media format type as a BSTR.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get_MediaFormatType method","IComponentType.get_MediaFormatType","IComponentType::get_MediaFormatType","IComponentTypeget_MediaFormatType","get_MediaFormatType","get_MediaFormatType method [Microsoft TV Technologies]","get_MediaFormatType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get_mediaformattype","tuner/IComponentType::get_MediaFormatType"]
old-location: mstv\icomponenttype_get_mediaformattype.htm
tech.root: mstv
ms.assetid: 5b618f33-2ef8-420b-9a15-83e1899476bc
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaFormatType method, IComponentType.get_MediaFormatType, IComponentType::get_MediaFormatType, IComponentTypeget_MediaFormatType, get_MediaFormatType, get_MediaFormatType method [Microsoft TV Technologies], get_MediaFormatType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediaformattype, tuner/IComponentType::get_MediaFormatType
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
 - IComponentType::get_MediaFormatType
 - tuner/IComponentType::get_MediaFormatType
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
 - IComponentType.get_MediaFormatType
---

# IComponentType::get_MediaFormatType


## -description

The <b>get_MediaFormatType</b> method retrieves the DirectShow media format type as a <b>BSTR</b>.

## -parameters

### -param MediaFormatType [out]

Pointer to a <b>BSTR</b> that will receive the GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>