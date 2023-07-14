---
UID: NF:tuner.IComponentType.get_MediaType
title: IComponentType::get_MediaType (tuner.h)
description: The get_MediaType method retrieves the DirectShow AM_MEDIA_TYPE structure for the component.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get_MediaType method","IComponentType.get_MediaType","IComponentType::get_MediaType","IComponentTypeget_MediaType","get_MediaType","get_MediaType method [Microsoft TV Technologies]","get_MediaType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get_mediatype","tuner/IComponentType::get_MediaType"]
old-location: mstv\icomponenttype_get_mediatype.htm
tech.root: mstv
ms.assetid: ca13cfc0-3e51-41cd-9405-aaa96927a35c
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaType method, IComponentType.get_MediaType, IComponentType::get_MediaType, IComponentTypeget_MediaType, get_MediaType, get_MediaType method [Microsoft TV Technologies], get_MediaType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediatype, tuner/IComponentType::get_MediaType
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
 - IComponentType::get_MediaType
 - tuner/IComponentType::get_MediaType
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
 - IComponentType.get_MediaType
---

# IComponentType::get_MediaType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MediaType</b> method retrieves the DirectShow <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure for the component.

## -parameters

### -param MediaType [out]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that will be filled in with the values associated with the current <a href="/previous-versions/windows/desktop/legacy/dd693036(v=vs.85)">ComponentType</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>