---
UID: NF:mfmediaengine.IMFMediaEngine.GetPlayed
title: IMFMediaEngine::GetPlayed (mfmediaengine.h)
description: Gets the time ranges that have been rendered.
helpviewer_keywords: ["GetPlayed","GetPlayed method [Media Foundation]","GetPlayed method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetPlayed method","IMFMediaEngine.GetPlayed","IMFMediaEngine::GetPlayed","mf.imfmediaengine_getplayed","mfmediaengine/IMFMediaEngine::GetPlayed"]
old-location: mf\imfmediaengine_getplayed.htm
tech.root: mf
ms.assetid: E74D1785-E8BA-4B3A-9FF8-63FBDED5FA9E
ms.date: 12/05/2018
ms.keywords: GetPlayed, GetPlayed method [Media Foundation], GetPlayed method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetPlayed method, IMFMediaEngine.GetPlayed, IMFMediaEngine::GetPlayed, mf.imfmediaengine_getplayed, mfmediaengine/IMFMediaEngine::GetPlayed
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
 - IMFMediaEngine::GetPlayed
 - mfmediaengine/IMFMediaEngine::GetPlayed
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
 - IMFMediaEngine.GetPlayed
---

# IMFMediaEngine::GetPlayed


## -description

Gets the time ranges that have been rendered.

## -parameters

### -param ppPlayed [out]

Receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>played</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>