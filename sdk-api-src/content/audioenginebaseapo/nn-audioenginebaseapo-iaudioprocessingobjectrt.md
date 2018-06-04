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

# IAudioProcessingObjectRT interface


## -description


This interface can operate in real-time mode and its methods can be called form real-time processing threads. The implementation of the methods for this interface must not block or touch paged memory. Additionally, you must not call any blocking system routines in the implementation of the methods.

The <code>IAudioProcessingObjectRT</code> interface includes the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536506">IAudioProcessingObjectRT::APOProcess</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536507">IAudioProcessingObjectRT::CalcInputFrames</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536508">IAudioProcessingObjectRT::CalcOutputFrames</a>


</dd>
</dl>
