---
UID: NF:audioengineendpoint.IAudioLfxControl.SetLocalEffectsState
title: IAudioLfxControl::SetLocalEffectsState
author: windows-sdk-content
description: The SetLocalEffectsState method sets the local effects state that is to be applied to the offloaded audio stream.
old-location: coreaudio\iaudiolfxcontrol_setlocaleffectsstate.htm
tech.root: CoreAudio
ms.assetid: F89C2610-BC71-4309-BCDA-5529B16A3FA7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAudioLfxControl interface [Core Audio],SetLocalEffectsState method, IAudioLfxControl.SetLocalEffectsState, IAudioLfxControl::SetLocalEffectsState, SetLocalEffectsState, SetLocalEffectsState method [Core Audio], SetLocalEffectsState method [Core Audio],IAudioLfxControl interface, audioengineendpoint/IAudioLfxControl::SetLocalEffectsState, coreaudio.iaudiolfxcontrol_setlocaleffectsstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Audioengineendpoint.h
api_name:
 - IAudioLfxControl.SetLocalEffectsState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioLfxControl::SetLocalEffectsState


## -description


The <b>SetLocalEffectsState</b> method sets the local effects state that is to be  applied to the offloaded audio stream.


## -parameters




### -param bEnabled [in]

Indicates the local effects state that is to be applied to the offloaded audio stream. A value of <b>TRUE</b> enables  local effects, and the local effects in the audio graph are applied to the stream. A value of <b>FALSE</b> disables local effects, so that the  local effects in the audio graph are not applied to the audio stream.


## -returns



The <b>SetLocalEffectsState</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/E4290AE9-7F2E-4D0B-BEAF-F01D95B3E03D">IAudioLfxControl</a>
 

 

