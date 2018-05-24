---
UID: NF:mfidl.IMFVideoProcessorControl2.EnableHardwareEffects
title: IMFVideoProcessorControl2::EnableHardwareEffects
author: windows-driver-content
description: Enables effects that were implemented with IDirectXVideoProcessor::VideoProcessorBlt.
old-location: mf\imfvideoprocessorcontrol2_enablehardwareeffects.htm
old-project: medfound
ms.assetid: 682B1FAA-05D5-40E3-98BD-DDEFB0C5B4AF
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: EnableHardwareEffects, EnableHardwareEffects method [Media Foundation], EnableHardwareEffects method [Media Foundation],IMFVideoProcessorControl2 interface, IMFVideoProcessorControl2 interface [Media Foundation],EnableHardwareEffects method, IMFVideoProcessorControl2.EnableHardwareEffects, IMFVideoProcessorControl2::EnableHardwareEffects, mf.imfvideoprocessorcontrol2_enablehardwareeffects, mfidl/IMFVideoProcessorControl2::EnableHardwareEffects
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFVideoProcessorControl2.EnableHardwareEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFVideoProcessorControl2::EnableHardwareEffects


## -description


Enables effects that were implemented with <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">IDirectXVideoProcessor::VideoProcessorBlt</a>. 


## -parameters




### -param fEnabled [in]

Type: <b>BOOL</b>

Specifies whether effects are to be enabled. <b>TRUE</b> specifies to enable effects. <b>FALSE</b> specifies to disable effects.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FE314254-AAE4-482E-A7AE-28B2591E0060">IMFVideoProcessorControl2</a>
 

 

