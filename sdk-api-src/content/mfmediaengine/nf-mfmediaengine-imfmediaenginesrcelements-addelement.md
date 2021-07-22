---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.AddElement
title: IMFMediaEngineSrcElements::AddElement (mfmediaengine.h)
description: Adds a source element to the end of the list.
helpviewer_keywords: ["AddElement","AddElement method [Media Foundation]","AddElement method [Media Foundation]","IMFMediaEngineSrcElements interface","IMFMediaEngineSrcElements interface [Media Foundation]","AddElement method","IMFMediaEngineSrcElements.AddElement","IMFMediaEngineSrcElements::AddElement","mf.imfmediaenginesrcelements_addelement","mfmediaengine/IMFMediaEngineSrcElements::AddElement"]
old-location: mf\imfmediaenginesrcelements_addelement.htm
tech.root: mf
ms.assetid: 2C98A70B-F6B3-4CA7-8D04-958DFCCD2A50
ms.date: 12/05/2018
ms.keywords: AddElement, AddElement method [Media Foundation], AddElement method [Media Foundation],IMFMediaEngineSrcElements interface, IMFMediaEngineSrcElements interface [Media Foundation],AddElement method, IMFMediaEngineSrcElements.AddElement, IMFMediaEngineSrcElements::AddElement, mf.imfmediaenginesrcelements_addelement, mfmediaengine/IMFMediaEngineSrcElements::AddElement
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
 - IMFMediaEngineSrcElements::AddElement
 - mfmediaengine/IMFMediaEngineSrcElements::AddElement
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
 - IMFMediaEngineSrcElements.AddElement
---

# IMFMediaEngineSrcElements::AddElement


## -description

Adds a source element to the end of the list.

## -parameters

### -param pURL [in]

The URL of the source element, or <b>NULL</b>.

### -param pType [in]

The MIME type of the source element, or <b>NULL</b>.

### -param pMedia [in]

A media-query string that specifies the intended media type, or <b>NULL</b>. If specified, the string should conform to the W3C <i>Media Queries</i> specification.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any of the parameters to this method can be <b>NULL</b>.

This method allocates copies of the <b>BSTR</b>s that are passed in.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a>