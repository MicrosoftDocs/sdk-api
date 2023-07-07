---
UID: NF:tuner.IComponentType.put_MediaSubType
title: IComponentType::put_MediaSubType (tuner.h)
description: The put_MediaSubType method sets the DirectShow media subtype.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put_MediaSubType method","IComponentType.put_MediaSubType","IComponentType::put_MediaSubType","IComponentTypeput_MediaSubType","mstv.icomponenttype_put_mediasubtype","put_MediaSubType","put_MediaSubType method [Microsoft TV Technologies]","put_MediaSubType method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put_MediaSubType"]
old-location: mstv\icomponenttype_put_mediasubtype.htm
tech.root: mstv
ms.assetid: dc635134-33da-4197-966a-5cb64315cb7c
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaSubType method, IComponentType.put_MediaSubType, IComponentType::put_MediaSubType, IComponentTypeput_MediaSubType, mstv.icomponenttype_put_mediasubtype, put_MediaSubType, put_MediaSubType method [Microsoft TV Technologies], put_MediaSubType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaSubType
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
 - IComponentType::put_MediaSubType
 - tuner/IComponentType::put_MediaSubType
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
 - IComponentType.put_MediaSubType
---

# IComponentType::put_MediaSubType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MediaSubType</b> method sets the DirectShow media subtype.

## -parameters

### -param MediaSubType [in]

<b>BSTR</b> that specifies the GUID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>