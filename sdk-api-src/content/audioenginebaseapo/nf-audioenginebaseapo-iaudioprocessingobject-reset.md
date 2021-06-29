---
UID: NF:audioenginebaseapo.IAudioProcessingObject.Reset
title: IAudioProcessingObject::Reset (audioenginebaseapo.h)
description: The Reset method resets the APO to its original state. This method does not cause any changes in the connection objects that are attached to the input or the output of the APO.
helpviewer_keywords: ["IAudioProcessingObject interface [Audio Devices]","Reset method","IAudioProcessingObject.Reset","IAudioProcessingObject::Reset","Reset","Reset method [Audio Devices]","Reset method [Audio Devices]","IAudioProcessingObject interface","audio.iaudioprocessingobject_reset","audio_syseffects_r_1df1a787-30e1-4eda-adde-a0b4a813ac9b.xml","audioenginebaseapo/IAudioProcessingObject::Reset"]
old-location: audio\iaudioprocessingobject_reset.htm
tech.root: audio
ms.assetid: 9d8c13cb-012e-4b5e-a1fd-1c2e5b9200b8
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObject interface [Audio Devices],Reset method, IAudioProcessingObject.Reset, IAudioProcessingObject::Reset, Reset, Reset method [Audio Devices], Reset method [Audio Devices],IAudioProcessingObject interface, audio.iaudioprocessingobject_reset, audio_syseffects_r_1df1a787-30e1-4eda-adde-a0b4a813ac9b.xml, audioenginebaseapo/IAudioProcessingObject::Reset
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObject::Reset
 - audioenginebaseapo/IAudioProcessingObject::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObject.Reset
---

## -description

The Reset method resets the APO to its original state. This method does not cause any changes in the connection objects that are attached to the input or the output of the APO.



## -returns

The <code>Reset</code> method returns a value of S_OK when the call is completed successfully.

## -remarks

This method is not real-time compliant and must not be called from a real-time processing thread. The implementation of this method does not and must not touch paged memory. Additionally, it must not call any blocking system routines.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudioprocessingobject">IAudioProcessingObject</a>
