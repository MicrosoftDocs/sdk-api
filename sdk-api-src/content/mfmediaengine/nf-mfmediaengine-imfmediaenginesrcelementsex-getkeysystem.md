---
UID: NF:mfmediaengine.IMFMediaEngineSrcElementsEx.GetKeySystem
title: IMFMediaEngineSrcElementsEx::GetKeySystem (mfmediaengine.h)
description: Gets the key system for the given source element index.
helpviewer_keywords: ["GetKeySystem","GetKeySystem method [Media Foundation]","GetKeySystem method [Media Foundation]","IMFMediaEngineSrcElementsEx interface","IMFMediaEngineSrcElementsEx interface [Media Foundation]","GetKeySystem method","IMFMediaEngineSrcElementsEx.GetKeySystem","IMFMediaEngineSrcElementsEx::GetKeySystem","mf.imfmediaenginesrcelementsex_getkeysystem","mfmediaengine/IMFMediaEngineSrcElementsEx::GetKeySystem"]
old-location: mf\imfmediaenginesrcelementsex_getkeysystem.htm
tech.root: mf
ms.assetid: 5d8db178-a17d-4920-9eed-b2dfba9f05fc
ms.date: 12/05/2018
ms.keywords: GetKeySystem, GetKeySystem method [Media Foundation], GetKeySystem method [Media Foundation],IMFMediaEngineSrcElementsEx interface, IMFMediaEngineSrcElementsEx interface [Media Foundation],GetKeySystem method, IMFMediaEngineSrcElementsEx.GetKeySystem, IMFMediaEngineSrcElementsEx::GetKeySystem, mf.imfmediaenginesrcelementsex_getkeysystem, mfmediaengine/IMFMediaEngineSrcElementsEx::GetKeySystem
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
 - IMFMediaEngineSrcElementsEx::GetKeySystem
 - mfmediaengine/IMFMediaEngineSrcElementsEx::GetKeySystem
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
 - IMFMediaEngineSrcElementsEx.GetKeySystem
---

# IMFMediaEngineSrcElementsEx::GetKeySystem


## -description

Gets the key system for the given source element index.

## -parameters

### -param index

The source element index.

### -param pType

The MIME type of the source element.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex">IMFMediaEngineSrcElementsEx</a>