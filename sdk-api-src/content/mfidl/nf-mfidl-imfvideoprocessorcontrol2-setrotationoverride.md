---
UID: NF:mfidl.IMFVideoProcessorControl2.SetRotationOverride
title: IMFVideoProcessorControl2::SetRotationOverride (mfidl.h)
description: Overrides the rotation operation that is performed in the video processor.
helpviewer_keywords: ["IMFVideoProcessorControl2 interface [Media Foundation]","SetRotationOverride method","IMFVideoProcessorControl2.SetRotationOverride","IMFVideoProcessorControl2::SetRotationOverride","SetRotationOverride","SetRotationOverride method [Media Foundation]","SetRotationOverride method [Media Foundation]","IMFVideoProcessorControl2 interface","mf.imfvideoprocessorcontrol2_setrotationoverride","mfidl/IMFVideoProcessorControl2::SetRotationOverride"]
old-location: mf\imfvideoprocessorcontrol2_setrotationoverride.htm
tech.root: mf
ms.assetid: 408048CF-0443-4F09-8AB9-A9A2827EA749
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl2 interface [Media Foundation],SetRotationOverride method, IMFVideoProcessorControl2.SetRotationOverride, IMFVideoProcessorControl2::SetRotationOverride, SetRotationOverride, SetRotationOverride method [Media Foundation], SetRotationOverride method [Media Foundation],IMFVideoProcessorControl2 interface, mf.imfvideoprocessorcontrol2_setrotationoverride, mfidl/IMFVideoProcessorControl2::SetRotationOverride
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
 - IMFVideoProcessorControl2::SetRotationOverride
 - mfidl/IMFVideoProcessorControl2::SetRotationOverride
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
 - IMFVideoProcessorControl2.SetRotationOverride
---

# IMFVideoProcessorControl2::SetRotationOverride


## -description

Overrides the rotation operation that is performed in the video processor.

## -parameters

### -param uiRotation [in]

Type: <b>UINT</b>

Rotation value in degrees.  Typically, you can only use values from the <a href="/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat">MFVideoRotationFormat</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2">IMFVideoProcessorControl2</a>