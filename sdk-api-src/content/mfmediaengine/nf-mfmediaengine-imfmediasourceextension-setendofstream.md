---
UID: NF:mfmediaengine.IMFMediaSourceExtension.SetEndOfStream
title: IMFMediaSourceExtension::SetEndOfStream (mfmediaengine.h)
description: Indicate that the end of the media stream has been reached.
helpviewer_keywords: ["IMFMediaSourceExtension interface [Media Foundation]","SetEndOfStream method","IMFMediaSourceExtension.SetEndOfStream","IMFMediaSourceExtension::SetEndOfStream","SetEndOfStream","SetEndOfStream method [Media Foundation]","SetEndOfStream method [Media Foundation]","IMFMediaSourceExtension interface","mf.imfmediasourceextension_setendofstream","mfmediaengine/IMFMediaSourceExtension::SetEndOfStream"]
old-location: mf\imfmediasourceextension_setendofstream.htm
tech.root: mf
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceExtension interface [Media Foundation],SetEndOfStream method, IMFMediaSourceExtension.SetEndOfStream, IMFMediaSourceExtension::SetEndOfStream, SetEndOfStream, SetEndOfStream method [Media Foundation], SetEndOfStream method [Media Foundation],IMFMediaSourceExtension interface, mf.imfmediasourceextension_setendofstream, mfmediaengine/IMFMediaSourceExtension::SetEndOfStream
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
 - IMFMediaSourceExtension::SetEndOfStream
 - mfmediaengine/IMFMediaSourceExtension::SetEndOfStream
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
 - IMFMediaSourceExtension.SetEndOfStream
---

# IMFMediaSourceExtension::SetEndOfStream


## -description

Indicate that the end of the media stream has been reached.

## -parameters

### -param error [in]

Used to pass error information.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>



<a href="/windows/desktop/medfound/mf-mse-error">MF_MSE_ERROR</a>