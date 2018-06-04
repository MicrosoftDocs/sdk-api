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

# IAudioProcessingObjectRT::CalcOutputFrames


## -description


The <code>CalcOutputFrames</code> method returns the number of output frames that an APO requires for a given number of input frames.


## -parameters




### -param u32InputFrameCount [in]

This is a count of the number of input frames.


## -returns



The <code>CalcOutputFrames</code> method returns the number of output frames that an APO will generate for a given number of input frames.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
</table>
 




## -remarks



The <code>CalcOutputFrames</code> method can be called form a real-time processing thread. The implementation of this method must not block or touch paged memory and it should not call any system blocking routines.



