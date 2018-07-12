---
UID: NN:audioenginebaseapo.IAudioProcessingObjectConfiguration
title: IAudioProcessingObjectConfiguration
author: windows-sdk-content
description: The IAudioProcessingObjectConfiguration interface is used to configure the APO. This interface uses its methods to lock and unlock the APO for processing.
old-location: audio\iaudioprocessingobjectconfiguration.htm
old-project: audio
ms.assetid: 6311a5d1-b9d3-4c62-99aa-8feda32b4a2f
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IAudioProcessingObjectConfiguration, IAudioProcessingObjectConfiguration interface [Audio Devices], IAudioProcessingObjectConfiguration interface [Audio Devices],described, audio.iaudioprocessingobjectconfiguration, audio_syseffects_r_b3847e21-94ea-45b3-9ae4-ccdb83f262aa.xml, audioenginebaseapo/IAudioProcessingObjectConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
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
 - IAudioProcessingObjectConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# IAudioProcessingObjectConfiguration interface


## -description


The <code>IAudioProcessingObjectConfiguration</code> interface is used to configure the APO. This interface uses its methods to lock and unlock the APO for processing.

The <code>IAudioProcessingObjectConfiguration</code> interface supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536503">IAudioProcessingObjectConfiguration::LockForProcess</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536504">IAudioProcessingObjectConfiguration::UnlockForProcess</a>


</dd>
</dl>
