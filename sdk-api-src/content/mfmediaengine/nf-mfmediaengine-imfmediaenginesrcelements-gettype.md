---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.GetType
title: IMFMediaEngineSrcElements::GetType (mfmediaengine.h)
description: Gets the MIME type of an element in the list.
helpviewer_keywords: ["GetType","GetType method [Media Foundation]","GetType method [Media Foundation]","IMFMediaEngineSrcElements interface","IMFMediaEngineSrcElements interface [Media Foundation]","GetType method","IMFMediaEngineSrcElements.GetType","IMFMediaEngineSrcElements::GetType","mf.imfmediaenginesrcelements_gettype","mfmediaengine/IMFMediaEngineSrcElements::GetType"]
old-location: mf\imfmediaenginesrcelements_gettype.htm
tech.root: mf
ms.assetid: 7B788160-A342-48B4-A3F9-42F3BB83A24D
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Media Foundation], GetType method [Media Foundation],IMFMediaEngineSrcElements interface, IMFMediaEngineSrcElements interface [Media Foundation],GetType method, IMFMediaEngineSrcElements.GetType, IMFMediaEngineSrcElements::GetType, mf.imfmediaenginesrcelements_gettype, mfmediaengine/IMFMediaEngineSrcElements::GetType
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFMediaEngineSrcElements::GetType
 - mfmediaengine/IMFMediaEngineSrcElements::GetType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSrcElements.GetType
---

# IMFMediaEngineSrcElements::GetType


## -description

Gets the MIME type of an element in the list.

## -parameters

### -param index [in]

The zero-based index of the source element. To get the number of source elements, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-getlength">IMFMediaEngineSrcElements::GetLength</a>.

### -param pType [out]

Receives a <b>BSTR</b> that contains the MIME type. The caller must free the  <b>BSTR</b> by calling <b>SysFreeString</b>. If no MIME type is set, this parameter receives the value <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a>