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

# IMSVidVideoRenderer2::put_SuppressEffects


## -description


The <b>put_SuppressEffects</b> method sets preferences for power management and visual effects.


## -parameters




### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



If <i>bSuppress</i> equals VARIANT_TRUE, the Video Control does the following:

<ul>
<li>Disables font smoothing and the system-wide drop shadow effect. (Only when the Video Control is using hardware overlay.) This is useful if the application draws onto the overlay.</li>
<li>Disables the screen saver, and turns off power management for the display. This is useful to prevent the operating system from interrupting playback while the user is watching a program.</li>
</ul>
The Video Control restores the original system settings after it stops.

If <i>bSuppress</i> equals VARIANT_FALSE, the Video Control uses the existing system settings.




## -see-also




<a href="https://msdn.microsoft.com/caaa2cf1-15be-47dc-82db-06915a55ba03">IMSVidVideoRenderer2 Interface</a>



<a href="https://msdn.microsoft.com/ee7a5c92-bdae-4b67-9b2b-5fb4ae3a8fd7">IMSVidVideoRenderer::put_UsingOverlay</a>
 

 

