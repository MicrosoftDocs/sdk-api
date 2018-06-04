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

# IAudioClockAdjustment::SetSampleRate


## -description


The <b>SetSampleRate</b> method sets the sample rate of a stream.


## -parameters




### -param flSampleRate [in]


				   The new sample rate in frames per second.
				


## -returns



If the method succeeds, it returns S_OK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The sample rate is out of the range for the Audio Processing Object.

</td>
</tr>
</table>
 




## -remarks



This method must not be called from a real-time processing thread.
			
		    

The new sample rate will take effect after the current frame is done processing and will remain in effect until <b>SetSampleRate</b> is called again.
		The audio client must be initialized in shared-mode (AUDCLNT_SHAREMODE_SHARED), otherwise <b>SetSampleRate</b> fails. 




## -see-also




<a href="https://msdn.microsoft.com/7b2267c3-79f5-4ada-a7ce-78dd514f8487">AUDCLNT_STREAMFLAGS_XXX Constants</a>



<a href="https://msdn.microsoft.com/61d90fd9-6c73-4987-b424-1523f15ab023">IAudioClockAdjustment</a>
 

 

