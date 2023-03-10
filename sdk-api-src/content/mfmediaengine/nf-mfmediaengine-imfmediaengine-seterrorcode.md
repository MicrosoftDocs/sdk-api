---
UID: NF:mfmediaengine.IMFMediaEngine.SetErrorCode
title: IMFMediaEngine::SetErrorCode (mfmediaengine.h)
description: Sets the current error code.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetErrorCode method","IMFMediaEngine.SetErrorCode","IMFMediaEngine::SetErrorCode","SetErrorCode","SetErrorCode method [Media Foundation]","SetErrorCode method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_seterrorcode","mfmediaengine/IMFMediaEngine::SetErrorCode"]
old-location: mf\imfmediaengine_seterrorcode.htm
tech.root: mf
ms.assetid: B40AFD99-1048-44C5-A3FA-ED57720956B4
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetErrorCode method, IMFMediaEngine.SetErrorCode, IMFMediaEngine::SetErrorCode, SetErrorCode, SetErrorCode method [Media Foundation], SetErrorCode method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_seterrorcode, mfmediaengine/IMFMediaEngine::SetErrorCode
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
 - IMFMediaEngine::SetErrorCode
 - mfmediaengine/IMFMediaEngine::SetErrorCode
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
 - IMFMediaEngine.SetErrorCode
---

# IMFMediaEngine::SetErrorCode


## -description

Sets the current error code.

## -parameters

### -param error [in]

The error code, as an <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_err">MF_MEDIA_ENGINE_ERR</a> value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>