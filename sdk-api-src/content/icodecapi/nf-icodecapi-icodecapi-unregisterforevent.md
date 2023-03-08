---
UID: NF:icodecapi.ICodecAPI.UnregisterForEvent
title: ICodecAPI::UnregisterForEvent
ms.date: 09/22/2020
targetos: Windows
description: The UnregisterForEvent method unregisters the application for a specified encoder event. (ICodecAPI::UnregisterForEvent)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","UnregisterForEvent method","ICodecAPI.UnregisterForEvent","ICodecAPI::UnregisterForEvent","ICodecAPIUnregisterForEvent","UnregisterForEvent","UnregisterForEvent method [DirectShow]","UnregisterForEvent method [DirectShow]","ICodecAPI interface","dshow.icodecapi_unregisterforevent","icodecapi/ICodecAPI::UnregisterForEvent"]
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icodecapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - icodecapi.h
api_name:
 - ICodecAPI::UnregisterForEvent
f1_keywords:
 - ICodecAPI::UnregisterForEvent
 - icodecapi/ICodecAPI::UnregisterForEvent
dev_langs:
 - c++
---

## -description

The <b>UnregisterForEvent</b> method unregisters the application for a specified encoder event.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the event.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks


<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/icodecapi/nn-icodecapi-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a>

## -see-also

