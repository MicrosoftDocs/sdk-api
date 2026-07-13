---
UID: NF:mfmediaengine.IMFMediaError.SetExtendedErrorCode
title: IMFMediaError::SetExtendedErrorCode (mfmediaengine.h)
description: Sets the extended error code.
helpviewer_keywords: ["IMFMediaError interface [Media Foundation]","SetExtendedErrorCode method","IMFMediaError.SetExtendedErrorCode","IMFMediaError::SetExtendedErrorCode","SetExtendedErrorCode","SetExtendedErrorCode method [Media Foundation]","SetExtendedErrorCode method [Media Foundation]","IMFMediaError interface","mf.imfmediaerror_setextendederrorcode","mfmediaengine/IMFMediaError::SetExtendedErrorCode"]
old-location: mf\imfmediaerror_setextendederrorcode.htm
tech.root: mf
ms.assetid: F3B52C1A-E235-492D-93C2-393FF2321B7E
ms.date: 12/05/2018
ms.keywords: IMFMediaError interface [Media Foundation],SetExtendedErrorCode method, IMFMediaError.SetExtendedErrorCode, IMFMediaError::SetExtendedErrorCode, SetExtendedErrorCode, SetExtendedErrorCode method [Media Foundation], SetExtendedErrorCode method [Media Foundation],IMFMediaError interface, mf.imfmediaerror_setextendederrorcode, mfmediaengine/IMFMediaError::SetExtendedErrorCode
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
 - IMFMediaError::SetExtendedErrorCode
 - mfmediaengine/IMFMediaError::SetExtendedErrorCode
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
 - IMFMediaError.SetExtendedErrorCode
---

# IMFMediaError::SetExtendedErrorCode


## -description

Sets the extended error code.

## -parameters

### -param error [in]

An <b>HRESULT</b> value that gives additional information about the last error.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror">IMFMediaError</a>