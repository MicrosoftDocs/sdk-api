---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.GetRequiredProtections
title: IMFMediaEngineProtectedContent::GetRequiredProtections (mfmediaengine.h)
description: Gets the content protections that must be applied in frame-server mode.
helpviewer_keywords: ["GetRequiredProtections","GetRequiredProtections method [Media Foundation]","GetRequiredProtections method [Media Foundation]","IMFMediaEngineProtectedContent interface","IMFMediaEngineProtectedContent interface [Media Foundation]","GetRequiredProtections method","IMFMediaEngineProtectedContent.GetRequiredProtections","IMFMediaEngineProtectedContent::GetRequiredProtections","mf.imfmediaengineprotectedcontent_getrequiredprotections","mfmediaengine/IMFMediaEngineProtectedContent::GetRequiredProtections"]
old-location: mf\imfmediaengineprotectedcontent_getrequiredprotections.htm
tech.root: mf
ms.assetid: 4D67813D-F222-4EB1-B059-6DB5EC642DA2
ms.date: 12/05/2018
ms.keywords: GetRequiredProtections, GetRequiredProtections method [Media Foundation], GetRequiredProtections method [Media Foundation],IMFMediaEngineProtectedContent interface, IMFMediaEngineProtectedContent interface [Media Foundation],GetRequiredProtections method, IMFMediaEngineProtectedContent.GetRequiredProtections, IMFMediaEngineProtectedContent::GetRequiredProtections, mf.imfmediaengineprotectedcontent_getrequiredprotections, mfmediaengine/IMFMediaEngineProtectedContent::GetRequiredProtections
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
 - IMFMediaEngineProtectedContent::GetRequiredProtections
 - mfmediaengine/IMFMediaEngineProtectedContent::GetRequiredProtections
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
 - IMFMediaEngineProtectedContent.GetRequiredProtections
---

# IMFMediaEngineProtectedContent::GetRequiredProtections


## -description

Gets the content protections that must be applied in frame-server mode.

## -parameters

### -param pFrameProtectionFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_frame_protection_flags">MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>