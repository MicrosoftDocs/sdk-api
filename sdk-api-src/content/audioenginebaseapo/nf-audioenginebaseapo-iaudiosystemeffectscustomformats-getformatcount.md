---
UID: NF:audioenginebaseapo.IAudioSystemEffectsCustomFormats.GetFormatCount
title: IAudioSystemEffectsCustomFormats::GetFormatCount
author: windows-sdk-content
description: The GetFormatCount method retrieves the number of custom formats supported by the system effects audio processing object (sAPO).
old-location: audio\iaudiosystemeffectscustomformats_getformatcount.htm
old-project: audio
ms.assetid: 70d215e5-e30a-4fbd-b9c3-c988c6bbd941
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFormatCount, GetFormatCount method [Audio Devices], GetFormatCount method [Audio Devices],IAudioSystemEffectsCustomFormats interface, IAudioSystemEffectsCustomFormats interface [Audio Devices],GetFormatCount method, IAudioSystemEffectsCustomFormats.GetFormatCount, IAudioSystemEffectsCustomFormats::GetFormatCount, audio.iaudiosystemeffectscustomformats_getformatcount, audio_syseffects_r_1f186185-3eb9-4683-a2e1-bbcc9598943d.xml, audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormatCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioenginebaseapo.h
req.include-header: Audioenginebaseapo.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
tech.root: 
req.typenames: APO_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioSystemEffectsCustomFormats.GetFormatCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# IAudioSystemEffectsCustomFormats::GetFormatCount


## -description


The <code>GetFormatCount</code> method retrieves the number of custom formats supported by the system effects audio processing object (sAPO).


## -parameters




### -param pcFormats [out]

Specifies a pointer to an unsigned integer. The unsigned integer represents the number of formats supported by the sAPO.


## -returns



The <code>GetFormatCount</code> method returns S_OK when the call is successful. Otherwise, it returns E_POINTER to indicate that an invalid pointer was passed to the function.




## -remarks



For more information about sAPOs, see <a href="https://msdn.microsoft.com/5275e404-19b9-4a44-88de-1a40f3798ede">System Effects Audio Processing Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/54ac63b4-9846-44ce-8afb-ded52ae2cd71">System Effects Audio Processing Objects</a>
 

 

