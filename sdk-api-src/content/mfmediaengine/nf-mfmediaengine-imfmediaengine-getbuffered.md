---
UID: NF:mfmediaengine.IMFMediaEngine.GetBuffered
title: IMFMediaEngine::GetBuffered (mfmediaengine.h)
description: Queries how much resource data the media engine has buffered.
helpviewer_keywords: ["GetBuffered","GetBuffered method [Media Foundation]","GetBuffered method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetBuffered method","IMFMediaEngine.GetBuffered","IMFMediaEngine::GetBuffered","mf.imfmediaengine_getbuffered","mfmediaengine/IMFMediaEngine::GetBuffered"]
old-location: mf\imfmediaengine_getbuffered.htm
tech.root: mf
ms.assetid: 38DABEE7-04AF-4542-AF4D-7988C824EA11
ms.date: 12/05/2018
ms.keywords: GetBuffered, GetBuffered method [Media Foundation], GetBuffered method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetBuffered method, IMFMediaEngine.GetBuffered, IMFMediaEngine::GetBuffered, mf.imfmediaengine_getbuffered, mfmediaengine/IMFMediaEngine::GetBuffered
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
 - IMFMediaEngine::GetBuffered
 - mfmediaengine/IMFMediaEngine::GetBuffered
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
 - IMFMediaEngine.GetBuffered
---

# IMFMediaEngine::GetBuffered


## -description

Queries how much resource data the media engine has buffered.

## -parameters

### -param ppBuffered [out]

Receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>buffered</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The returned  <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a> interface represents a list of time ranges. The time ranges indicate which portions of the media resource have been downloaded. The time range list can be empty.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>