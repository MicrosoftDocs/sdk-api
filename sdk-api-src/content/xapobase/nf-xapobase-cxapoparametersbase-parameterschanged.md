---
UID: NF:xapobase.CXAPOParametersBase.ParametersChanged
title: CXAPOParametersBase::ParametersChanged (xapobase.h)
description: Indicates if IXAPOParameters::SetParameters has been called since the last processing pass.
helpviewer_keywords: ["CXAPOParametersBase interface [XAudio2 Audio Mixing APIs]","ParametersChanged method","CXAPOParametersBase.ParametersChanged","CXAPOParametersBase::ParametersChanged","ParametersChanged","ParametersChanged method [XAudio2 Audio Mixing APIs]","ParametersChanged method [XAudio2 Audio Mixing APIs]","CXAPOParametersBase interface","xapobase/CXAPOParametersBase::ParametersChanged","xaudio2.cxapoparametersbase_parameterschanged"]
old-location: xaudio2\cxapoparametersbase_parameterschanged.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.ParametersChanged
ms.date: 12/05/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],ParametersChanged method, CXAPOParametersBase.ParametersChanged, CXAPOParametersBase::ParametersChanged, ParametersChanged, ParametersChanged method [XAudio2 Audio Mixing APIs], ParametersChanged method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::ParametersChanged, xaudio2.cxapoparametersbase_parameterschanged
req.header: xapobase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CXAPOParametersBase::ParametersChanged
 - xapobase/CXAPOParametersBase::ParametersChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOParametersBase.ParametersChanged
---

# CXAPOParametersBase::ParametersChanged


## -description

Indicates if <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> has been called since the last processing pass.



## -returns

Returns TRUE if <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> has been called since the last processing pass. May only be used within the XAPO's <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> implementation, before <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess">CXAPOParametersBase::BeginProcess</a> is called.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a>
