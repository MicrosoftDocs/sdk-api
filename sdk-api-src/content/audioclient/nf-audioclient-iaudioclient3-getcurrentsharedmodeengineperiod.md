---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAudioClient3::GetCurrentSharedModeEnginePeriod


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
 

 

