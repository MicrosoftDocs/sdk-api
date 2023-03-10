---
UID: NF:mfmediaengine.IMFMediaError.SetErrorCode
title: IMFMediaError::SetErrorCode (mfmediaengine.h)
description: Sets the error code.
helpviewer_keywords: ["IMFMediaError interface [Media Foundation]","SetErrorCode method","IMFMediaError.SetErrorCode","IMFMediaError::SetErrorCode","SetErrorCode","SetErrorCode method [Media Foundation]","SetErrorCode method [Media Foundation]","IMFMediaError interface","mf.imfmediaerror_seterrorcode","mfmediaengine/IMFMediaError::SetErrorCode"]
old-location: mf\imfmediaerror_seterrorcode.htm
tech.root: mf
ms.assetid: 0CEFC8A5-CCEA-43CF-80AB-C9862B0DAEDA
ms.date: 12/05/2018
ms.keywords: IMFMediaError interface [Media Foundation],SetErrorCode method, IMFMediaError.SetErrorCode, IMFMediaError::SetErrorCode, SetErrorCode, SetErrorCode method [Media Foundation], SetErrorCode method [Media Foundation],IMFMediaError interface, mf.imfmediaerror_seterrorcode, mfmediaengine/IMFMediaError::SetErrorCode
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
 - IMFMediaError::SetErrorCode
 - mfmediaengine/IMFMediaError::SetErrorCode
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
 - IMFMediaError.SetErrorCode
---

# IMFMediaError::SetErrorCode


## -description

Sets the error code.

## -parameters

### -param error [in]

The error code, specified as an <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_err">MF_MEDIA_ENGINE_ERR</a> value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror">IMFMediaError</a>