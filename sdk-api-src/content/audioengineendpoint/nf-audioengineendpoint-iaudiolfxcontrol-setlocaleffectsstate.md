---
UID: NF:audioengineendpoint.IAudioLfxControl.SetLocalEffectsState
title: IAudioLfxControl::SetLocalEffectsState (audioengineendpoint.h)
description: The SetLocalEffectsState method sets the local effects state that is to be applied to the offloaded audio stream.
helpviewer_keywords: ["IAudioLfxControl interface [Core Audio]","SetLocalEffectsState method","IAudioLfxControl.SetLocalEffectsState","IAudioLfxControl::SetLocalEffectsState","SetLocalEffectsState","SetLocalEffectsState method [Core Audio]","SetLocalEffectsState method [Core Audio]","IAudioLfxControl interface","audioengineendpoint/IAudioLfxControl::SetLocalEffectsState","coreaudio.iaudiolfxcontrol_setlocaleffectsstate"]
old-location: coreaudio\iaudiolfxcontrol_setlocaleffectsstate.htm
tech.root: CoreAudio
ms.assetid: F89C2610-BC71-4309-BCDA-5529B16A3FA7
ms.date: 12/05/2018
ms.keywords: IAudioLfxControl interface [Core Audio],SetLocalEffectsState method, IAudioLfxControl.SetLocalEffectsState, IAudioLfxControl::SetLocalEffectsState, SetLocalEffectsState, SetLocalEffectsState method [Core Audio], SetLocalEffectsState method [Core Audio],IAudioLfxControl interface, audioengineendpoint/IAudioLfxControl::SetLocalEffectsState, coreaudio.iaudiolfxcontrol_setlocaleffectsstate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioLfxControl::SetLocalEffectsState
 - audioengineendpoint/IAudioLfxControl::SetLocalEffectsState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioLfxControl.SetLocalEffectsState
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

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiolfxcontrol">IAudioLfxControl</a>