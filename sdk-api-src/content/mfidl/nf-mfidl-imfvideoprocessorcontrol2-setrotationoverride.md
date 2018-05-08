---
UID: NF:mfidl.IMFVideoProcessorControl2.SetRotationOverride
title: IMFVideoProcessorControl2::SetRotationOverride
author: windows-driver-content
description: Overrides the rotation operation that is performed in the video processor.
old-location: mf\imfvideoprocessorcontrol2_setrotationoverride.htm
old-project: medfound
ms.assetid: 408048CF-0443-4F09-8AB9-A9A2827EA749
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFVideoProcessorControl2 interface [Media Foundation],SetRotationOverride method, IMFVideoProcessorControl2.SetRotationOverride, IMFVideoProcessorControl2::SetRotationOverride, SetRotationOverride, SetRotationOverride method [Media Foundation], SetRotationOverride method [Media Foundation],IMFVideoProcessorControl2 interface, mf.imfvideoprocessorcontrol2_setrotationoverride, mfidl/IMFVideoProcessorControl2::SetRotationOverride
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFVideoProcessorControl2.SetRotationOverride
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl2::SetRotationOverride


## -description


Overrides the rotation operation that is performed in the video processor.


## -parameters




### -param uiRotation [in]

Type: <b>UINT</b>

Rotation value in degrees.  Typically, you can only use values from the <a href="https://msdn.microsoft.com/E2760742-3914-4B5C-87FB-38F2EF3025C3">MFVideoRotationFormat</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FE314254-AAE4-482E-A7AE-28B2591E0060">IMFVideoProcessorControl2</a>
 

 

