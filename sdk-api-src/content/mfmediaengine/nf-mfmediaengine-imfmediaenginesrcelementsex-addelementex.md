---
UID: NF:mfmediaengine.IMFMediaEngineSrcElementsEx.AddElementEx
title: IMFMediaEngineSrcElementsEx::AddElementEx (mfmediaengine.h)
description: Provides an enhanced version of IMFMediaEngineSrcElements::AddElement to add the key system intended to be used with content to an element.
helpviewer_keywords: ["AddElementEx","AddElementEx method [Media Foundation]","AddElementEx method [Media Foundation]","IMFMediaEngineSrcElementsEx interface","IMFMediaEngineSrcElementsEx interface [Media Foundation]","AddElementEx method","IMFMediaEngineSrcElementsEx.AddElementEx","IMFMediaEngineSrcElementsEx::AddElementEx","mf.imfmediaenginesrcelementsex_addelementex","mfmediaengine/IMFMediaEngineSrcElementsEx::AddElementEx"]
old-location: mf\imfmediaenginesrcelementsex_addelementex.htm
tech.root: mf
ms.assetid: ad799c61-3ffb-4879-a875-d218c0b56e1c
ms.date: 12/05/2018
ms.keywords: AddElementEx, AddElementEx method [Media Foundation], AddElementEx method [Media Foundation],IMFMediaEngineSrcElementsEx interface, IMFMediaEngineSrcElementsEx interface [Media Foundation],AddElementEx method, IMFMediaEngineSrcElementsEx.AddElementEx, IMFMediaEngineSrcElementsEx::AddElementEx, mf.imfmediaenginesrcelementsex_addelementex, mfmediaengine/IMFMediaEngineSrcElementsEx::AddElementEx
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaEngineSrcElementsEx::AddElementEx
 - mfmediaengine/IMFMediaEngineSrcElementsEx::AddElementEx
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
 - IMFMediaEngineSrcElementsEx.AddElementEx
---

# IMFMediaEngineSrcElementsEx::AddElementEx


## -description

Provides an enhanced version of <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-addelement">IMFMediaEngineSrcElements::AddElement</a> to add the key system intended to be used with content to an element.

## -parameters

### -param pURL

The URL of the source element, or <b>NULL</b>.

### -param pType

The MIME type of the source element, or <b>NULL</b>.

### -param pMedia

A media-query string that specifies the intended media type, or <b>NULL</b>. If specified, the string should conform to the W3C <i>Media Queries</i> specification.

### -param keySystem

The media key session.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex">IMFMediaEngineSrcElementsEx</a>