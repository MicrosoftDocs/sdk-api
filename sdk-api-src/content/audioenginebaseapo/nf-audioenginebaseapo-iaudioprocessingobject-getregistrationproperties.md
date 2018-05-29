---
UID: NF:audioenginebaseapo.IAudioProcessingObject.GetRegistrationProperties
title: IAudioProcessingObject::GetRegistrationProperties
author: windows-sdk-content
description: GetRegistrationProperties returns the registration properties of the audio processing object (APO).
old-location: audio\iaudioprocessingobject_getregistrationproperties.htm
old-project: audio
ms.assetid: A0D0BAA9-7942-4952-AC9D-087EE7FE6DD0
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetRegistrationProperties, GetRegistrationProperties method [Audio Devices], GetRegistrationProperties method [Audio Devices],IAudioProcessingObject interface, IAudioProcessingObject interface [Audio Devices],GetRegistrationProperties method, IAudioProcessingObject.GetRegistrationProperties, IAudioProcessingObject::GetRegistrationProperties, audio.iaudioprocessingobject_getregistrationproperties, audioenginebaseapo/IAudioProcessingObject::GetRegistrationProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows 7 and later Windows operating systems.
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
req.typenames: APO_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioenginebaseapo.idl
-	Audioenginebaseapo.idl.dll
api_name:
-	IAudioProcessingObject.GetRegistrationProperties
product: Windows
targetos: Windows
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: Any level
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
 

 

