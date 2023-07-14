---
UID: NF:tuner.IComponentType.put__MediaMajorType
title: IComponentType::put__MediaMajorType (tuner.h)
description: The put__MediaMajorType method sets the DirectShow media major type.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put__MediaMajorType method","IComponentType.put__MediaMajorType","IComponentType::put__MediaMajorType","IComponentTypeput__MediaMajorType","mstv.icomponenttype_put__mediamajortype","put__MediaMajorType","put__MediaMajorType method [Microsoft TV Technologies]","put__MediaMajorType method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put__MediaMajorType"]
old-location: mstv\icomponenttype_put__mediamajortype.htm
tech.root: mstv
ms.assetid: 3886f7fe-1520-4fee-a88b-26ee1cdf32fe
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put__MediaMajorType method, IComponentType.put__MediaMajorType, IComponentType::put__MediaMajorType, IComponentTypeput__MediaMajorType, mstv.icomponenttype_put__mediamajortype, put__MediaMajorType, put__MediaMajorType method [Microsoft TV Technologies], put__MediaMajorType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put__MediaMajorType
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
 - IComponentType::put__MediaMajorType
 - tuner/IComponentType::put__MediaMajorType
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
 - IComponentType.put__MediaMajorType
---

# IComponentType::put__MediaMajorType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put__MediaMajorType</b> method sets the DirectShow media major type.

## -parameters

### -param MediaMajorTypeGuid [in]

<b>REFCLSID</b> that specifies the media major type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>