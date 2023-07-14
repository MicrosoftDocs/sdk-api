---
UID: NF:tuner.IComponentType.put_MediaMajorType
title: IComponentType::put_MediaMajorType (tuner.h)
description: The put_MediaMajorType method sets the DirectShow media major type.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put_MediaMajorType method","IComponentType.put_MediaMajorType","IComponentType::put_MediaMajorType","IComponentTypeput_MediaMajorType","mstv.icomponenttype_put_mediamajortype","put_MediaMajorType","put_MediaMajorType method [Microsoft TV Technologies]","put_MediaMajorType method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put_MediaMajorType"]
old-location: mstv\icomponenttype_put_mediamajortype.htm
tech.root: mstv
ms.assetid: 455a51f4-eb01-437a-9cb9-6ff93a6cc76e
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaMajorType method, IComponentType.put_MediaMajorType, IComponentType::put_MediaMajorType, IComponentTypeput_MediaMajorType, mstv.icomponenttype_put_mediamajortype, put_MediaMajorType, put_MediaMajorType method [Microsoft TV Technologies], put_MediaMajorType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaMajorType
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
 - IComponentType::put_MediaMajorType
 - tuner/IComponentType::put_MediaMajorType
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
 - IComponentType.put_MediaMajorType
---

# IComponentType::put_MediaMajorType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MediaMajorType</b> method sets the DirectShow media major type.

## -parameters

### -param MediaMajorType [in]

<b>BSTR</b> that specifies the GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>