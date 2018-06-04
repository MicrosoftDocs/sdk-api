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

# IAudioProcessingObject interface


## -description


System Effects Audio Processing Objects (sAPOs) are typically used in or called from real-time process threads. However, it is sometimes necessary to use an sAPO in a non real-time mode. For example, when an sAPO is initialized, it is called from a non real-time thread. But when audio processing begins, the sAPO is called from a real-time thread. The <code>IAudioProcessingObject</code> interface exposes methods that enable a client to access the non real-time compliant parts of an sAPO.

The <code>IAudioProcessingObject</code> interface supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/6DB8B945-DCED-4129-A457-E90E083E6394">IAudioProcessingObject::GetInputChannelCount</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536509">IAudioProcessingObject::GetLatency</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/A0D0BAA9-7942-4952-AC9D-087EE7FE6DD0">IAudioProcessingObject::GetRegistrationProperties</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536510">IAudioProcessingObject::Initialize</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536511">IAudioProcessingObject::IsInputFormatSupported</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536512">IAudioProcessingObject::IsOutputFormatSupported</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536513">IAudioProcessingObject::Reset</a>


</dd>
</dl>
