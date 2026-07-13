---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetPresentationAttribute
title: IMFMediaEngineEx::GetPresentationAttribute (mfmediaengine.h)
description: Gets a presentation attribute from the media resource.
helpviewer_keywords: ["GetPresentationAttribute","GetPresentationAttribute method [Media Foundation]","GetPresentationAttribute method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetPresentationAttribute method","IMFMediaEngineEx.GetPresentationAttribute","IMFMediaEngineEx::GetPresentationAttribute","mf.imfmediaengineex_getpresentationattribute","mfmediaengine/IMFMediaEngineEx::GetPresentationAttribute"]
old-location: mf\imfmediaengineex_getpresentationattribute.htm
tech.root: mf
ms.assetid: 127667EA-8ED2-428E-8F6B-C280CF42E1C5
ms.date: 12/05/2018
ms.keywords: GetPresentationAttribute, GetPresentationAttribute method [Media Foundation], GetPresentationAttribute method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetPresentationAttribute method, IMFMediaEngineEx.GetPresentationAttribute, IMFMediaEngineEx::GetPresentationAttribute, mf.imfmediaengineex_getpresentationattribute, mfmediaengine/IMFMediaEngineEx::GetPresentationAttribute
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
 - IMFMediaEngineEx::GetPresentationAttribute
 - mfmediaengine/IMFMediaEngineEx::GetPresentationAttribute
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
 - IMFMediaEngineEx.GetPresentationAttribute
---

# IMFMediaEngineEx::GetPresentationAttribute


## -description

Gets a presentation attribute from the media resource.

## -parameters

### -param guidMFAttribute [in]

The attribute to query.

For a list of presentation attributes, see <a href="/windows/desktop/medfound/presentation-descriptor-attributes">Presentation Descriptor Attributes</a>.

### -param pvValue [out]

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. The caller must free the <b>PROPVARIANT</b> by calling <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>