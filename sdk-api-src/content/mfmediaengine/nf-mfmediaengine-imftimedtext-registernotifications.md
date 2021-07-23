---
UID: NF:mfmediaengine.IMFTimedText.RegisterNotifications
title: IMFTimedText::RegisterNotifications (mfmediaengine.h)
description: Registers a timed-text notify object.
helpviewer_keywords: ["IMFTimedText interface [Media Foundation]","RegisterNotifications method","IMFTimedText.RegisterNotifications","IMFTimedText::RegisterNotifications","RegisterNotifications","RegisterNotifications method [Media Foundation]","RegisterNotifications method [Media Foundation]","IMFTimedText interface","mf.imftimedtext_registernotifications","mfmediaengine/IMFTimedText::RegisterNotifications"]
old-location: mf\imftimedtext_registernotifications.htm
tech.root: mf
ms.assetid: 0C43CD34-22A2-440A-97D5-682D979B52A9
ms.date: 12/05/2018
ms.keywords: IMFTimedText interface [Media Foundation],RegisterNotifications method, IMFTimedText.RegisterNotifications, IMFTimedText::RegisterNotifications, RegisterNotifications, RegisterNotifications method [Media Foundation], RegisterNotifications method [Media Foundation],IMFTimedText interface, mf.imftimedtext_registernotifications, mfmediaengine/IMFTimedText::RegisterNotifications
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IMFTimedText::RegisterNotifications
 - mfmediaengine/IMFTimedText::RegisterNotifications
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
 - IMFTimedText.RegisterNotifications
---

# IMFTimedText::RegisterNotifications


## -description

Registers a timed-text notify object.

## -parameters

### -param notify [in, optional]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify">IMFTimedTextNotify</a>*</b>

A pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify">IMFTimedTextNotify</a> interface for the timed-text notify object to register.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>