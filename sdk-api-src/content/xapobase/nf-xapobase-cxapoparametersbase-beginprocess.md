---
UID: NF:xapobase.CXAPOParametersBase.BeginProcess
title: CXAPOParametersBase::BeginProcess (xapobase.h)
description: Returns the current process parameters.
helpviewer_keywords: ["BeginProcess","BeginProcess method [XAudio2 Audio Mixing APIs]","BeginProcess method [XAudio2 Audio Mixing APIs]","CXAPOParametersBase interface","CXAPOParametersBase interface [XAudio2 Audio Mixing APIs]","BeginProcess method","CXAPOParametersBase.BeginProcess","CXAPOParametersBase::BeginProcess","xapobase/CXAPOParametersBase::BeginProcess","xaudio2.cxapoparametersbase_beginprocess"]
old-location: xaudio2\cxapoparametersbase_beginprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.BeginProcess
ms.date: 12/05/2018
ms.keywords: BeginProcess, BeginProcess method [XAudio2 Audio Mixing APIs], BeginProcess method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],BeginProcess method, CXAPOParametersBase.BeginProcess, CXAPOParametersBase::BeginProcess, xapobase/CXAPOParametersBase::BeginProcess, xaudio2.cxapoparametersbase_beginprocess
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
 - CXAPOParametersBase::BeginProcess
 - xapobase/CXAPOParametersBase::BeginProcess
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
 - CXAPOParametersBase.BeginProcess
---

# CXAPOParametersBase::BeginProcess


## -description

Returns the current process parameters.



## -returns

Returns a pointer to the current process parameters.

## -remarks

XAPOs must call this method within their <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> implementation to access the current process parameters in a thread-safe manner.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a>
