---
UID: NF:mfidl.IMFVideoProcessorControl2.GetSupportedHardwareEffects
title: IMFVideoProcessorControl2::GetSupportedHardwareEffects (mfidl.h)
description: Returns the list of supported effects in the currently configured video processor.
helpviewer_keywords: ["GetSupportedHardwareEffects","GetSupportedHardwareEffects method [Media Foundation]","GetSupportedHardwareEffects method [Media Foundation]","IMFVideoProcessorControl2 interface","IMFVideoProcessorControl2 interface [Media Foundation]","GetSupportedHardwareEffects method","IMFVideoProcessorControl2.GetSupportedHardwareEffects","IMFVideoProcessorControl2::GetSupportedHardwareEffects","mf.imfvideoprocessorcontrol2_getsupportedhardwareeffects","mfidl/IMFVideoProcessorControl2::GetSupportedHardwareEffects"]
old-location: mf\imfvideoprocessorcontrol2_getsupportedhardwareeffects.htm
tech.root: mf
ms.assetid: 0D5FE2B8-B8DD-40DE-8B41-40E773976BE6
ms.date: 12/05/2018
ms.keywords: GetSupportedHardwareEffects, GetSupportedHardwareEffects method [Media Foundation], GetSupportedHardwareEffects method [Media Foundation],IMFVideoProcessorControl2 interface, IMFVideoProcessorControl2 interface [Media Foundation],GetSupportedHardwareEffects method, IMFVideoProcessorControl2.GetSupportedHardwareEffects, IMFVideoProcessorControl2::GetSupportedHardwareEffects, mf.imfvideoprocessorcontrol2_getsupportedhardwareeffects, mfidl/IMFVideoProcessorControl2::GetSupportedHardwareEffects
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
 - IMFVideoProcessorControl2::GetSupportedHardwareEffects
 - mfidl/IMFVideoProcessorControl2::GetSupportedHardwareEffects
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
 - IMFVideoProcessorControl2.GetSupportedHardwareEffects
---

# IMFVideoProcessorControl2::GetSupportedHardwareEffects


## -description

Returns the list of supported effects in the currently configured video processor.

## -parameters

### -param puiSupport [out]

Type: <b>UINT*</b>

A combination of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps">D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the list of supported effect capabilities.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2">IMFVideoProcessorControl2</a>