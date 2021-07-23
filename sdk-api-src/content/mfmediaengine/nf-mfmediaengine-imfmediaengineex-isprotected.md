---
UID: NF:mfmediaengine.IMFMediaEngineEx.IsProtected
title: IMFMediaEngineEx::IsProtected (mfmediaengine.h)
description: Queries whether the media resource contains protected content.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","IsProtected method","IMFMediaEngineEx.IsProtected","IMFMediaEngineEx::IsProtected","IsProtected","IsProtected method [Media Foundation]","IsProtected method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_isprotected","mfmediaengine/IMFMediaEngineEx::IsProtected"]
old-location: mf\imfmediaengineex_isprotected.htm
tech.root: mf
ms.assetid: 704C469D-C8C7-48D7-B41E-4475B4A9181D
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],IsProtected method, IMFMediaEngineEx.IsProtected, IMFMediaEngineEx::IsProtected, IsProtected, IsProtected method [Media Foundation], IsProtected method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_isprotected, mfmediaengine/IMFMediaEngineEx::IsProtected
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
 - IMFMediaEngineEx::IsProtected
 - mfmediaengine/IMFMediaEngineEx::IsProtected
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
 - IMFMediaEngineEx.IsProtected
---

# IMFMediaEngineEx::IsProtected


## -description

Queries whether the media resource contains protected content.

## -parameters

### -param pProtected [out]

Receives the value <b>TRUE</b> if the media resource contains protected content, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>