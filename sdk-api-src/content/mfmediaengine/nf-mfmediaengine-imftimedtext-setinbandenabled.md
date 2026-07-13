---
UID: NF:mfmediaengine.IMFTimedText.SetInBandEnabled
title: IMFTimedText::SetInBandEnabled (mfmediaengine.h)
description: Enables or disables inband mode.
helpviewer_keywords: ["IMFTimedText interface [Media Foundation]","SetInBandEnabled method","IMFTimedText.SetInBandEnabled","IMFTimedText::SetInBandEnabled","SetInBandEnabled","SetInBandEnabled method [Media Foundation]","SetInBandEnabled method [Media Foundation]","IMFTimedText interface","mf.imftimedtext_setinbandenabled","mfmediaengine/IMFTimedText::SetInBandEnabled"]
old-location: mf\imftimedtext_setinbandenabled.htm
tech.root: mf
ms.assetid: 4AF63D30-4A91-4DFF-96B9-0A26102B93FE
ms.date: 12/05/2018
ms.keywords: IMFTimedText interface [Media Foundation],SetInBandEnabled method, IMFTimedText.SetInBandEnabled, IMFTimedText::SetInBandEnabled, SetInBandEnabled, SetInBandEnabled method [Media Foundation], SetInBandEnabled method [Media Foundation],IMFTimedText interface, mf.imftimedtext_setinbandenabled, mfmediaengine/IMFTimedText::SetInBandEnabled
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
 - IMFTimedText::SetInBandEnabled
 - mfmediaengine/IMFTimedText::SetInBandEnabled
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
 - IMFTimedText.SetInBandEnabled
---

# IMFTimedText::SetInBandEnabled


## -description

Enables or disables inband mode.

## -parameters

### -param enabled [in]

Type: <b>BOOL</b>

Specifies whether inband mode is enabled. If <b>TRUE</b>, inband mode is enabled. If <b>FALSE</b>, inband mode is disabled.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>