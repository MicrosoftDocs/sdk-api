---
UID: NF:mfmediaengine.IMFMediaKeySession.GetError
title: IMFMediaKeySession::GetError (mfmediaengine.h)
description: Gets the error state associated with the media key session.
helpviewer_keywords: ["GetError","GetError method [Media Foundation]","GetError method [Media Foundation]","IMFMediaKeySession interface","IMFMediaKeySession interface [Media Foundation]","GetError method","IMFMediaKeySession.GetError","IMFMediaKeySession::GetError","mf.imfmediakeysession_geterror","mfmediaengine/IMFMediaKeySession::GetError"]
old-location: mf\imfmediakeysession_geterror.htm
tech.root: mf
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
ms.date: 12/05/2018
ms.keywords: GetError, GetError method [Media Foundation], GetError method [Media Foundation],IMFMediaKeySession interface, IMFMediaKeySession interface [Media Foundation],GetError method, IMFMediaKeySession.GetError, IMFMediaKeySession::GetError, mf.imfmediakeysession_geterror, mfmediaengine/IMFMediaKeySession::GetError
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
 - IMFMediaKeySession::GetError
 - mfmediaengine/IMFMediaKeySession::GetError
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
 - IMFMediaKeySession.GetError
---

# IMFMediaKeySession::GetError


## -description

Gets the error state associated with the media key session.

## -parameters

### -param code

The error code.

### -param systemCode

Platform specific error information.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession">IMFMediaKeySession</a>