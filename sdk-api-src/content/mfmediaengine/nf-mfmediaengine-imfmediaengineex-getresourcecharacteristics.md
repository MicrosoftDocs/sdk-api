---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetResourceCharacteristics
title: IMFMediaEngineEx::GetResourceCharacteristics (mfmediaengine.h)
description: Gets various flags that describe the media resource.
helpviewer_keywords: ["GetResourceCharacteristics","GetResourceCharacteristics method [Media Foundation]","GetResourceCharacteristics method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetResourceCharacteristics method","IMFMediaEngineEx.GetResourceCharacteristics","IMFMediaEngineEx::GetResourceCharacteristics","mf.imfmediaengineex_getresourcecharacteristics","mfmediaengine/IMFMediaEngineEx::GetResourceCharacteristics"]
old-location: mf\imfmediaengineex_getresourcecharacteristics.htm
tech.root: mf
ms.assetid: 534595D7-007F-450B-A1C7-FA08F3958417
ms.date: 12/05/2018
ms.keywords: GetResourceCharacteristics, GetResourceCharacteristics method [Media Foundation], GetResourceCharacteristics method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetResourceCharacteristics method, IMFMediaEngineEx.GetResourceCharacteristics, IMFMediaEngineEx::GetResourceCharacteristics, mf.imfmediaengineex_getresourcecharacteristics, mfmediaengine/IMFMediaEngineEx::GetResourceCharacteristics
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
 - IMFMediaEngineEx::GetResourceCharacteristics
 - mfmediaengine/IMFMediaEngineEx::GetResourceCharacteristics
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
 - IMFMediaEngineEx.GetResourceCharacteristics
---

# IMFMediaEngineEx::GetResourceCharacteristics


## -description

Gets various flags that describe the media resource.

## -parameters

### -param pCharacteristics [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics">MFMEDIASOURCE_CHARACTERISTICS enumeration</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>