---
UID: NF:audioenginebaseapo.IAudioProcessingObjectConfiguration.UnlockForProcess
title: IAudioProcessingObjectConfiguration::UnlockForProcess (audioenginebaseapo.h)
description: The UnlockForProcess method releases the lock that was imposed on the APO by the LockForProcess method.
helpviewer_keywords: ["IAudioProcessingObjectConfiguration interface [Audio Devices]","UnlockForProcess method","IAudioProcessingObjectConfiguration.UnlockForProcess","IAudioProcessingObjectConfiguration::UnlockForProcess","UnlockForProcess","UnlockForProcess method [Audio Devices]","UnlockForProcess method [Audio Devices]","IAudioProcessingObjectConfiguration interface","audio.iaudioprocessingobjectconfiguration_unlockforprocess","audio_syseffects_r_23133166-d468-4449-82e1-2fba54e220c6.xml","audioenginebaseapo/IAudioProcessingObjectConfiguration::UnlockForProcess"]
old-location: audio\iaudioprocessingobjectconfiguration_unlockforprocess.htm
tech.root: audio
ms.assetid: 54221040-71b8-4b31-81df-46435f7b2b80
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObjectConfiguration interface [Audio Devices],UnlockForProcess method, IAudioProcessingObjectConfiguration.UnlockForProcess, IAudioProcessingObjectConfiguration::UnlockForProcess, UnlockForProcess, UnlockForProcess method [Audio Devices], UnlockForProcess method [Audio Devices],IAudioProcessingObjectConfiguration interface, audio.iaudioprocessingobjectconfiguration_unlockforprocess, audio_syseffects_r_23133166-d468-4449-82e1-2fba54e220c6.xml, audioenginebaseapo/IAudioProcessingObjectConfiguration::UnlockForProcess
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available Windows Vista and later versions of the Windows operating system.
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
 - IAudioProcessingObjectConfiguration::UnlockForProcess
 - audioenginebaseapo/IAudioProcessingObjectConfiguration::UnlockForProcess
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
 - IAudioProcessingObjectConfiguration.UnlockForProcess
---

## -description

The <code>UnlockForProcess</code> method releases the lock that was imposed on the APO by the LockForProcess method.



## -returns

The <code>UnlockForProcess</code> method returns a value of S_OK if the call completed successfully. If the APO was already unlocked when the call was made, the method returns a value of APOERR_ALREADY_UNLOCKED.

## -remarks

The <code>UnlockForProcess</code> method places the APO in a mode that makes configuration changes possible. These changes include Add, Remove, and Swap of the input and output connections that are attached to the APO.

