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

# IAudioProcessingObject::GetRegistrationProperties


## -description


GetRegistrationProperties returns the registration properties of the audio processing object (APO).
<div class="alert"><b>Note</b>  Starting with Windows 8.1, this method has been deprecated.</div><div> </div>

## -parameters




### -param ppRegProps [out]

The registration properties of the APO. This parameter is of type <a href="https://msdn.microsoft.com/library/windows/hardware/dn425140">APO_REG_PROPERTIES</a>.


## -returns



<code>GetRegistrationProperties</code> returns a 

value of S_OK if the call was successful. Otherwise, it returns an error code of E_POINTER to indicate that an invalid pointer was passed to the function.




## -remarks



The caller must free the memory returned by <code>GetRegistrationProperties</code>.

<div class="alert"><b>Note</b>  <p class="note">This method must not be called from a real-time processing thread.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536501">IAudioProcessingObject</a>
 

 

