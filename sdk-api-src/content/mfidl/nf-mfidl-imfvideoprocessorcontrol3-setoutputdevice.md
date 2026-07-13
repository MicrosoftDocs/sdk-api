---
UID: NF:mfidl.IMFVideoProcessorControl3.SetOutputDevice
tech.root: mf
title: IMFVideoProcessorControl3::SetOutputDevice
ms.date: 09/09/2025
targetos: Windows
description: Sets the output device when the video processor is used as part of a renderer and the renderer has knowledge of the output device.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1803
req.target-min-winversvr: Windows Server version 1803
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl3::SetOutputDevice
f1_keywords:
 - IMFVideoProcessorControl3::SetOutputDevice
 - mfidl/IMFVideoProcessorControl3::SetOutputDevice
dev_langs:
 - c++
helpviewer_keywords:
 - SetOutputDevice
---

## -description

Sets the output device when the video processor is used as part of a renderer and the renderer has knowledge of the output device.

## -parameters

### -param pOutputDevice [in]

An **IUnknown** representing the output device.  This may be either a [IDXGIOutput](/windows/win32/api/dxgi/nn-dxgi-idxgioutput) or [Windows.Graphics.Display.IDisplayInformation](/uwp/api/windows.graphics.display.displayinformation), depending on the renderer.


## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

