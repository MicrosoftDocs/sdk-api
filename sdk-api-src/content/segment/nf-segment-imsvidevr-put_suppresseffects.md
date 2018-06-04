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

# IMSVidEVR::put_SuppressEffects


## -description


The <b>put_SuppressEffects</b> method specifies whether the <a href="https://msdn.microsoft.com/743a1950-4f70-45a1-9536-0d75064f401b">Video Control</a> configures the system for optimal video playback.


## -parameters




### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If <i>bSuppress</i> equals VARIANT_TRUE, the Video Control configures several system parameters during video playback:

<ul>
<li>Disables the screen saver timeout.</li>
<li>Disables Microsoft ClearType smoothing.</li>
<li>Disables the drop shadow effect.</li>
<li>Disables alpha-blended mouse cursors.</li>
<li>Prevents the system from turning off the display (power management).</li>
</ul>
For applications based on the Windows Graphics Device Interface (GDI), these settings improve the video playback experience. When playback stops, the Video Control restores the original system settings.

If <i>bSuppress</i> equals VARIANT_FALSE, the Video Control does not modify any of these system settings.

The default value for this property is VARIANT_TRUE. Set this property to VARIANT_FALSE if your application wants to control all of the system settings; for example, if you are providing a custom presenter.




## -see-also




<a href="https://msdn.microsoft.com/437f515b-0353-4ff2-b8c2-5dd27d4e12f7">IMSVidEVR</a>
 

 

