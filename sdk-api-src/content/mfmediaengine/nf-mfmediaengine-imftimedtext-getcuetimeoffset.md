---
UID: NF:mfmediaengine.IMFTimedText.GetCueTimeOffset
title: IMFTimedText::GetCueTimeOffset (mfmediaengine.h)
description: Gets the offset to the cue time.
helpviewer_keywords: ["GetCueTimeOffset","GetCueTimeOffset method [Media Foundation]","GetCueTimeOffset method [Media Foundation]","IMFTimedText interface","IMFTimedText interface [Media Foundation]","GetCueTimeOffset method","IMFTimedText.GetCueTimeOffset","IMFTimedText::GetCueTimeOffset","mf.imftimedtext_getcuetimeoffset","mfmediaengine/IMFTimedText::GetCueTimeOffset"]
old-location: mf\imftimedtext_getcuetimeoffset.htm
tech.root: mf
ms.assetid: E7619B18-6253-41CF-9D4D-F7944A8E5DDE
ms.date: 12/05/2018
ms.keywords: GetCueTimeOffset, GetCueTimeOffset method [Media Foundation], GetCueTimeOffset method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetCueTimeOffset method, IMFTimedText.GetCueTimeOffset, IMFTimedText::GetCueTimeOffset, mf.imftimedtext_getcuetimeoffset, mfmediaengine/IMFTimedText::GetCueTimeOffset
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
 - IMFTimedText::GetCueTimeOffset
 - mfmediaengine/IMFTimedText::GetCueTimeOffset
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
 - IMFTimedText.GetCueTimeOffset
---

# IMFTimedText::GetCueTimeOffset


## -description

Gets the offset to the cue time.

## -parameters

### -param offset [out]

Type: <b>double*</b>

A pointer to a variable that receives the offset to the cue time.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>