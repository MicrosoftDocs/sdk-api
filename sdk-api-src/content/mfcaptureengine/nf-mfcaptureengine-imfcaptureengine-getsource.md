---
UID: NF:mfcaptureengine.IMFCaptureEngine.GetSource
title: IMFCaptureEngine::GetSource (mfcaptureengine.h)
description: Gets a pointer to the capture source object.
helpviewer_keywords: ["GetSource","GetSource method [Media Foundation]","GetSource method [Media Foundation]","IMFCaptureEngine interface","IMFCaptureEngine interface [Media Foundation]","GetSource method","IMFCaptureEngine.GetSource","IMFCaptureEngine::GetSource","mf.imfcaptureengine_getsource","mfcaptureengine/IMFCaptureEngine::GetSource"]
old-location: mf\imfcaptureengine_getsource.htm
tech.root: mf
ms.assetid: 9DED11CA-BDBB-4E1A-BAD1-2EB6216543F9
ms.date: 12/05/2018
ms.keywords: GetSource, GetSource method [Media Foundation], GetSource method [Media Foundation],IMFCaptureEngine interface, IMFCaptureEngine interface [Media Foundation],GetSource method, IMFCaptureEngine.GetSource, IMFCaptureEngine::GetSource, mf.imfcaptureengine_getsource, mfcaptureengine/IMFCaptureEngine::GetSource
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFCaptureEngine::GetSource
 - mfcaptureengine/IMFCaptureEngine::GetSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine.GetSource
---

# IMFCaptureEngine::GetSource


## -description

Gets a pointer to the capture source object. Use the capture source to configure the capture devices.

## -parameters

### -param ppSource [out]

Receives a pointer to the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource">IMFCaptureSource</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>