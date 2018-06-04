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

# IMSVidVMR9::put_SuppressEffects


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>put_SuppressEffects</b> method specifies whether the Video Control configures the system for optimal video playback.


## -parameters




### -param bSuppress [in]

Specifies a Boolean value. See Remarks for more information.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




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

The default value for this property is VARIANT_TRUE. Set this property to VARIANT_FALSE if your application wants to control all of the system settings; for example, if you are providing a custom allocator-presenter (see <a href="https://msdn.microsoft.com/f654adac-12b6-47c7-99d4-0612b1532df4">IMSVidVMR9::SetAllocator</a>).




## -see-also




<a href="https://msdn.microsoft.com/c96f91d4-fc6c-4422-8fc9-ea5fed10bd80">IMSVidVMR9 Interface</a>
 

 

