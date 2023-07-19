---
UID: NF:tuner.IComponentType.get__MediaFormatType
title: IComponentType::get__MediaFormatType (tuner.h)
description: The get__MediaFormatType method retrieves the DirectShow media format type as a GUID.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get__MediaFormatType method","IComponentType.get__MediaFormatType","IComponentType::get__MediaFormatType","IComponentTypeget__MediaFormatType","get__MediaFormatType","get__MediaFormatType method [Microsoft TV Technologies]","get__MediaFormatType method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get__mediaformattype","tuner/IComponentType::get__MediaFormatType"]
old-location: mstv\icomponenttype_get__mediaformattype.htm
tech.root: mstv
ms.assetid: 21dccb42-8430-4fa0-a549-98dd3d1a4d4c
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get__MediaFormatType method, IComponentType.get__MediaFormatType, IComponentType::get__MediaFormatType, IComponentTypeget__MediaFormatType, get__MediaFormatType, get__MediaFormatType method [Microsoft TV Technologies], get__MediaFormatType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get__mediaformattype, tuner/IComponentType::get__MediaFormatType
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
 - IComponentType::get__MediaFormatType
 - tuner/IComponentType::get__MediaFormatType
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
 - IComponentType.get__MediaFormatType
---

# IComponentType::get__MediaFormatType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__MediaFormatType</b> method retrieves the DirectShow media format type as a GUID.

## -parameters

### -param MediaFormatTypeGuid [out]

Pointer to a GUID that will receive the format type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>