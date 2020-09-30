---
UID: NF:xapobase.CXAPOParametersBase.OnSetParameters
title: CXAPOParametersBase::OnSetParameters (xapobase.h)
description: Called by IXAPOParameters::SetParameters to allow for user-defined parameter validation.
helpviewer_keywords: ["CXAPOParametersBase interface [XAudio2 Audio Mixing APIs]","OnSetParameters method","CXAPOParametersBase.OnSetParameters","CXAPOParametersBase::OnSetParameters","OnSetParameters","OnSetParameters method [XAudio2 Audio Mixing APIs]","OnSetParameters method [XAudio2 Audio Mixing APIs]","CXAPOParametersBase interface","xapobase/CXAPOParametersBase::OnSetParameters","xaudio2.cxapoparametersbase_onsetparameters"]
old-location: xaudio2\cxapoparametersbase_onsetparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.OnSetParameters(const void,UINT32)
ms.date: 12/05/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],OnSetParameters method, CXAPOParametersBase.OnSetParameters, CXAPOParametersBase::OnSetParameters, OnSetParameters, OnSetParameters method [XAudio2 Audio Mixing APIs], OnSetParameters method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::OnSetParameters, xaudio2.cxapoparametersbase_onsetparameters
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
 - CXAPOParametersBase::OnSetParameters
 - xapobase/CXAPOParametersBase::OnSetParameters
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
 - CXAPOParametersBase.OnSetParameters
---

# CXAPOParametersBase::OnSetParameters


## -description

Called by <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> to allow for user-defined parameter validation.

## -parameters

### -param pParameters

Effect-specific parameter block.

### -param ParameterByteSize

Size, in bytes, of pParameters.

## -remarks

Users are expected to use asserts for parameter validation in <b>OnSetParameters</b>.



The <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a> class's implementation of <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> validates that <i>ParameterByteSize</i> is equal to the <b>m_uParameterBlockByteSize</b> private member before calling <b>OnSetParameters</b> so it may be assumed that <i>ParameterByteSize</i> == <b>m_uParameterBlockByteSize</b>. <b>m_uParameterBlockByteSize</b> will be equal to the <i>uParameterBlockByteSize</i> parameter passed into the <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapoparametersbase-cxapoparametersbase">CXAPOParametersBase::CXAPOParametersBase</a> constructor.



This method should not block as it is called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a>