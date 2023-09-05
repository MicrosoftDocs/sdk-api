---
UID: NF:tuner.IComponentType.get_MediaSubType
title: IComponentType::get_MediaSubType (tuner.h)
description: The get_MediaSubType method retrieves the DirectShow media subtype as a BSTR.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get_MediaSubType method","IComponentType.get_MediaSubType","IComponentType::get_MediaSubType","IComponentTypeget_MediaSubType","get_MediaSubType","get_MediaSubType method [Microsoft TV Technologies]","get_MediaSubType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get_mediasubtype","tuner/IComponentType::get_MediaSubType"]
old-location: mstv\icomponenttype_get_mediasubtype.htm
tech.root: mstv
ms.assetid: 470b7960-b016-4807-858b-61a53daf2396
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaSubType method, IComponentType.get_MediaSubType, IComponentType::get_MediaSubType, IComponentTypeget_MediaSubType, get_MediaSubType, get_MediaSubType method [Microsoft TV Technologies], get_MediaSubType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediasubtype, tuner/IComponentType::get_MediaSubType
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
 - IComponentType::get_MediaSubType
 - tuner/IComponentType::get_MediaSubType
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
 - IComponentType.get_MediaSubType
---

# IComponentType::get_MediaSubType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MediaSubType</b> method retrieves the DirectShow media subtype as a BSTR.

## -parameters

### -param MediaSubType [out]

Pointer to a <b>BSTR</b> that will receive the GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>