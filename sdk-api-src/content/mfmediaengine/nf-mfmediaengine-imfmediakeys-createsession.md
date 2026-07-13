---
UID: NF:mfmediaengine.IMFMediaKeys.CreateSession
title: IMFMediaKeys::CreateSession (mfmediaengine.h)
description: Creates a media key session object using the specified initialization data and custom data. .
helpviewer_keywords: ["CreateSession","CreateSession method [Media Foundation]","CreateSession method [Media Foundation]","IMFMediaKeys interface","IMFMediaKeys interface [Media Foundation]","CreateSession method","IMFMediaKeys.CreateSession","IMFMediaKeys::CreateSession","mf.imfmediakeys_createsession","mfmediaengine/IMFMediaKeys::CreateSession"]
old-location: mf\imfmediakeys_createsession.htm
tech.root: mf
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
ms.date: 12/05/2018
ms.keywords: CreateSession, CreateSession method [Media Foundation], CreateSession method [Media Foundation],IMFMediaKeys interface, IMFMediaKeys interface [Media Foundation],CreateSession method, IMFMediaKeys.CreateSession, IMFMediaKeys::CreateSession, mf.imfmediakeys_createsession, mfmediaengine/IMFMediaKeys::CreateSession
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
 - IMFMediaKeys::CreateSession
 - mfmediaengine/IMFMediaKeys::CreateSession
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
 - IMFMediaKeys.CreateSession
---

# IMFMediaKeys::CreateSession


## -description

Creates a media key session object using the specified initialization data and custom data.
.

## -parameters

### -param mimeType

The MIME type of the media container used for the content.

### -param initData

The initialization data for the key system.

### -param cb

The count in bytes of <i>initData</i>.

### -param customData

Custom data sent to the key system.

### -param cbCustomData

The count in bytes of <i>cbCustomData</i>.

### -param notify

notify

### -param ppSession

The media key session.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys">IMFMediaKeys</a>