---
UID: NF:audioclient.IAudioClient3.GetCurrentSharedModeEnginePeriod
title: IAudioClient3::GetCurrentSharedModeEnginePeriod method
author: windows-driver-content
description: Returns the current format and periodicity of the audio engine.
old-location: coreaudio\iaudioclient3_getcurrentsharedmodeengineperiod.htm
old-project: CoreAudio
ms.assetid: F91E46F5-5D12-4D53-842B-4495CAA3E09E
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetCurrentSharedModeEnginePeriod method [Core Audio], GetCurrentSharedModeEnginePeriod method [Core Audio], IAudioClient3 interface, GetCurrentSharedModeEnginePeriod,IAudioClient3.GetCurrentSharedModeEnginePeriod, IAudioClient3, IAudioClient3 interface [Core Audio], GetCurrentSharedModeEnginePeriod method, IAudioClient3::GetCurrentSharedModeEnginePeriod, audioclient/IAudioClient3::GetCurrentSharedModeEnginePeriod, coreaudio.iaudioclient3_getcurrentsharedmodeengineperiod
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audioclient.h
api_name:
-	IAudioClient3.GetCurrentSharedModeEnginePeriod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioClient3::GetCurrentSharedModeEnginePeriod method


## -description


Returns the current format and periodicity of the audio engine. This method enables audio clients to match the current period of the audio engine. 


## -parameters




### -param ppFormat [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>**</b>

The current device format that is being used by the audio engine.


### -param pCurrentPeriodInFrames [out]

Type: <b>UINT32*</b>

The current period of the audio engine, in audio frames.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code. 




## -remarks



<div class="alert"><b>Note</b>  The values returned by this method are instantaneous values and may be invalid immediately after the call returns if, for example, another audio client sets the periodicity or format to a different value.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/E8EFE682-E1BC-4D0D-A60E-DD257D6E5894">IAudioClient3</a>
 

 

