---
UID: NN:audioenginebaseapo.IAudioProcessingObject
title: IAudioProcessingObject
author: windows-sdk-content
description: System Effects Audio Processing Objects (sAPOs) are typically used in or called from real-time process threads.
old-location: audio\iaudioprocessingobject.htm
tech.root: audio
ms.assetid: 71be0151-20dd-40e3-a478-d67e4d8d9c36
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IAudioProcessingObject, IAudioProcessingObject interface [Audio Devices], IAudioProcessingObject interface [Audio Devices],described, audio.iaudioprocessingobject, audio_syseffects_r_7b8bb04d-2546-4fa3-ae7b-7e11df3b1e15.xml, audioenginebaseapo/IAudioProcessingObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioProcessingObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioProcessingObject interface


## -description


System Effects Audio Processing Objects (sAPOs) are typically used in or called from real-time process threads. However, it is sometimes necessary to use an sAPO in a non real-time mode. For example, when an sAPO is initialized, it is called from a non real-time thread. But when audio processing begins, the sAPO is called from a real-time thread. The <code>IAudioProcessingObject</code> interface exposes methods that enable a client to access the non real-time compliant parts of an sAPO.

The <code>IAudioProcessingObject</code> interface supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/6DB8B945-DCED-4129-A457-E90E083E6394">IAudioProcessingObject::GetInputChannelCount</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/7ac982cd-7fb7-4427-ac17-508bcc72391d">IAudioProcessingObject::GetLatency</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/A0D0BAA9-7942-4952-AC9D-087EE7FE6DD0">IAudioProcessingObject::GetRegistrationProperties</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/b73c2e18-ab7b-4e34-9440-f38891f99bf7">IAudioProcessingObject::Initialize</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/11eebb5d-21fd-48f7-8929-cd2612a3f451">IAudioProcessingObject::IsInputFormatSupported</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/19609332-9fc2-4a21-b947-f103a1cf2675">IAudioProcessingObject::IsOutputFormatSupported</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/9d8c13cb-012e-4b5e-a1fd-1c2e5b9200b8">IAudioProcessingObject::Reset</a>


</dd>
</dl>
