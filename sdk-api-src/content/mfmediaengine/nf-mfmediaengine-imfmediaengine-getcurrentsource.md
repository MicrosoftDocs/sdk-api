---
UID: NF:mfmediaengine.IMFMediaEngine.GetCurrentSource
title: IMFMediaEngine::GetCurrentSource (mfmediaengine.h)
description: Gets the URL of the current media resource, or an empty string if no media resource is present.
helpviewer_keywords: ["GetCurrentSource","GetCurrentSource method [Media Foundation]","GetCurrentSource method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetCurrentSource method","IMFMediaEngine.GetCurrentSource","IMFMediaEngine::GetCurrentSource","mf.imfmediaengine_getcurrentsource","mfmediaengine/IMFMediaEngine::GetCurrentSource"]
old-location: mf\imfmediaengine_getcurrentsource.htm
tech.root: mf
ms.assetid: 04C4281D-20ED-49B3-B00C-14ECF1E3BDE1
ms.date: 12/05/2018
ms.keywords: GetCurrentSource, GetCurrentSource method [Media Foundation], GetCurrentSource method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetCurrentSource method, IMFMediaEngine.GetCurrentSource, IMFMediaEngine::GetCurrentSource, mf.imfmediaengine_getcurrentsource, mfmediaengine/IMFMediaEngine::GetCurrentSource
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
 - IMFMediaEngine::GetCurrentSource
 - mfmediaengine/IMFMediaEngine::GetCurrentSource
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
 - IMFMediaEngine.GetCurrentSource
---

# IMFMediaEngine::GetCurrentSource


## -description

Gets the URL of the current media resource, or an empty string if no media resource is present.

## -parameters

### -param ppUrl [out]

Receives a <b>BSTR</b> that contains the URL of the current media resource. If there is no media resource, <i>ppUrl</i> receives an empty string. The caller must free the  <b>BSTR</b> by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>currentSrc</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

Initially, the current media resource is empty. It is updated when the Media Engine performs the resource selection algorithm.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>