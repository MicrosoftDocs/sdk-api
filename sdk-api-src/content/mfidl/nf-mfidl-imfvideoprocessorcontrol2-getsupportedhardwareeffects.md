---
UID: NF:mfidl.IMFVideoProcessorControl2.GetSupportedHardwareEffects
title: IMFVideoProcessorControl2::GetSupportedHardwareEffects
author: windows-sdk-content
description: Returns the list of supported effects in the currently configured video processor.
old-location: mf\imfvideoprocessorcontrol2_getsupportedhardwareeffects.htm
tech.root: medfound
ms.assetid: 0D5FE2B8-B8DD-40DE-8B41-40E773976BE6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSupportedHardwareEffects, GetSupportedHardwareEffects method [Media Foundation], GetSupportedHardwareEffects method [Media Foundation],IMFVideoProcessorControl2 interface, IMFVideoProcessorControl2 interface [Media Foundation],GetSupportedHardwareEffects method, IMFVideoProcessorControl2.GetSupportedHardwareEffects, IMFVideoProcessorControl2::GetSupportedHardwareEffects, mf.imfvideoprocessorcontrol2_getsupportedhardwareeffects, mfidl/IMFVideoProcessorControl2::GetSupportedHardwareEffects
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl2.GetSupportedHardwareEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoProcessorControl2::GetSupportedHardwareEffects


## -description


Returns the list of supported effects in the currently configured video processor.


## -parameters




### -param puiSupport [out]

Type: <b>UINT*</b>

A combination of <a href="https://msdn.microsoft.com/73836F8D-0A0C-4719-A27F-AC13617380D2">D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the list of suppported effect capabilities.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FE314254-AAE4-482E-A7AE-28B2591E0060">IMFVideoProcessorControl2</a>
 

 

