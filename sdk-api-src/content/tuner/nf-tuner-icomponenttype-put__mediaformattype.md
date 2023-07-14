---
UID: NF:tuner.IComponentType.put__MediaFormatType
title: IComponentType::put__MediaFormatType (tuner.h)
description: The put__MediaFormatType method sets the DirectShow media format type.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put__MediaFormatType method","IComponentType.put__MediaFormatType","IComponentType::put__MediaFormatType","IComponentTypeput__MediaFormatType","mstv.icomponenttype_put__mediaformattype","put__MediaFormatType","put__MediaFormatType method [Microsoft TV Technologies]","put__MediaFormatType method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put__MediaFormatType"]
old-location: mstv\icomponenttype_put__mediaformattype.htm
tech.root: mstv
ms.assetid: 37baa69e-d942-41d6-b497-bf37d6b0d57b
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put__MediaFormatType method, IComponentType.put__MediaFormatType, IComponentType::put__MediaFormatType, IComponentTypeput__MediaFormatType, mstv.icomponenttype_put__mediaformattype, put__MediaFormatType, put__MediaFormatType method [Microsoft TV Technologies], put__MediaFormatType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put__MediaFormatType
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
 - IComponentType::put__MediaFormatType
 - tuner/IComponentType::put__MediaFormatType
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
 - IComponentType.put__MediaFormatType
---

# IComponentType::put__MediaFormatType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put__MediaFormatType</b> method sets the DirectShow media format type.

## -parameters

### -param MediaFormatTypeGuid [in]

<b>REFCLSID</b> that specifies the media format type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>