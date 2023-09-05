---
UID: NF:tuner.IComponentType.get__MediaMajorType
title: IComponentType::get__MediaMajorType (tuner.h)
description: The get__MediaMajorType method retrieves the DirectShow media format type as a GUID.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get__MediaMajorType method","IComponentType.get__MediaMajorType","IComponentType::get__MediaMajorType","IComponentTypeget__MediaMajorType","get__MediaMajorType","get__MediaMajorType method [Microsoft TV Technologies]","get__MediaMajorType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get__mediamajortype","tuner/IComponentType::get__MediaMajorType"]
old-location: mstv\icomponenttype_get__mediamajortype.htm
tech.root: mstv
ms.assetid: b8732070-3560-461b-a04e-3c00d6b7b49e
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get__MediaMajorType method, IComponentType.get__MediaMajorType, IComponentType::get__MediaMajorType, IComponentTypeget__MediaMajorType, get__MediaMajorType, get__MediaMajorType method [Microsoft TV Technologies], get__MediaMajorType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get__mediamajortype, tuner/IComponentType::get__MediaMajorType
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
 - IComponentType::get__MediaMajorType
 - tuner/IComponentType::get__MediaMajorType
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
 - IComponentType.get__MediaMajorType
---

# IComponentType::get__MediaMajorType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__MediaMajorType</b> method retrieves the DirectShow media format type as a GUID.

## -parameters

### -param MediaMajorTypeGuid [out]

Pointer to a GUID that will receive the major type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>