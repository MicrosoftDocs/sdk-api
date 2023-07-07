---
UID: NF:tuner.IComponentType.get_MediaMajorType
title: IComponentType::get_MediaMajorType (tuner.h)
description: The get_MediaMajorType method retrieves the DirectShow media major type as a BSTR.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get_MediaMajorType method","IComponentType.get_MediaMajorType","IComponentType::get_MediaMajorType","IComponentTypeget_MediaMajorType","get_MediaMajorType","get_MediaMajorType method [Microsoft TV Technologies]","get_MediaMajorType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get_mediamajortype","tuner/IComponentType::get_MediaMajorType"]
old-location: mstv\icomponenttype_get_mediamajortype.htm
tech.root: mstv
ms.assetid: 4c1fc49d-acca-40fe-85cf-909092ceb5ef
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaMajorType method, IComponentType.get_MediaMajorType, IComponentType::get_MediaMajorType, IComponentTypeget_MediaMajorType, get_MediaMajorType, get_MediaMajorType method [Microsoft TV Technologies], get_MediaMajorType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediamajortype, tuner/IComponentType::get_MediaMajorType
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
 - IComponentType::get_MediaMajorType
 - tuner/IComponentType::get_MediaMajorType
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
 - IComponentType.get_MediaMajorType
---

# IComponentType::get_MediaMajorType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MediaMajorType</b> method retrieves the DirectShow media major type as a <b>BSTR</b>.

## -parameters

### -param MediaMajorType [out]

Pointer to a <b>BSTR</b> that will receive the GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>