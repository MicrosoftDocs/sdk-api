---
UID: NF:mfidl.IMFVideoProcessorControl2.EnableHardwareEffects
title: IMFVideoProcessorControl2::EnableHardwareEffects (mfidl.h)
description: Enables effects that were implemented with IDirectXVideoProcessor::VideoProcessorBlt.
helpviewer_keywords: ["EnableHardwareEffects","EnableHardwareEffects method [Media Foundation]","EnableHardwareEffects method [Media Foundation]","IMFVideoProcessorControl2 interface","IMFVideoProcessorControl2 interface [Media Foundation]","EnableHardwareEffects method","IMFVideoProcessorControl2.EnableHardwareEffects","IMFVideoProcessorControl2::EnableHardwareEffects","mf.imfvideoprocessorcontrol2_enablehardwareeffects","mfidl/IMFVideoProcessorControl2::EnableHardwareEffects"]
old-location: mf\imfvideoprocessorcontrol2_enablehardwareeffects.htm
tech.root: mf
ms.assetid: 682B1FAA-05D5-40E3-98BD-DDEFB0C5B4AF
ms.date: 12/05/2018
ms.keywords: EnableHardwareEffects, EnableHardwareEffects method [Media Foundation], EnableHardwareEffects method [Media Foundation],IMFVideoProcessorControl2 interface, IMFVideoProcessorControl2 interface [Media Foundation],EnableHardwareEffects method, IMFVideoProcessorControl2.EnableHardwareEffects, IMFVideoProcessorControl2::EnableHardwareEffects, mf.imfvideoprocessorcontrol2_enablehardwareeffects, mfidl/IMFVideoProcessorControl2::EnableHardwareEffects
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
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
 - IMFVideoProcessorControl2::EnableHardwareEffects
 - mfidl/IMFVideoProcessorControl2::EnableHardwareEffects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl2.EnableHardwareEffects
---

# IMFVideoProcessorControl2::EnableHardwareEffects


## -description

Enables effects that were implemented with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">IDirectXVideoProcessor::VideoProcessorBlt</a>.

## -parameters

### -param fEnabled [in]

Type: <b>BOOL</b>

Specifies whether effects are to be enabled. <b>TRUE</b> specifies to enable effects. <b>FALSE</b> specifies to disable effects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2">IMFVideoProcessorControl2</a>