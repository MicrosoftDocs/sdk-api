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

# IOleInPlaceSiteWindowless::SetFocus


## -description


Sets the keyboard focus for a UI-active, windowless object.


## -parameters




### -param fFocus [in]

If <b>TRUE</b>, sets the keyboard focus to the calling object. If <b>FALSE</b>, removes the keyboard focus from the calling object, provided that the object has the focus.


## -returns



This method returns S_OK if the keyboard focus was successfully given to the object. If this method is called to release the focus, it should never fail. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Keyboard focus was denied to the object.

</td>
</tr>
</table>
 




## -remarks



A windowless object calls this method whenever a windowed object would call the <a href="_win32_SetFocus_cpp">SetFocus</a> function. Through this call, the windowless object obtains the keyboard focus and can respond to window messages. Normally, this call is made during the UI activation process and within the notification methods <a href="https://msdn.microsoft.com/8333d707-4d34-4a87-9990-b25597ffa9fc">IOleInPlaceActiveObject::OnDocWindowActivate</a> with <b>TRUE</b> and <a href="https://msdn.microsoft.com/6534ea03-5f1b-4d3e-b6d8-b8d478a0a144">IOleInPlaceActiveObject::OnFrameWindowActivate</a> with <b>TRUE</b>.

In response to this call, the container sets the Windows focus to the window being used to get keyboard messages (usually the container window) and redirects any subsequent keyboard messages to the windowless object that requested the focus.

A windowless object also calls the <b>IOleInPlaceSiteWindowless::SetFocus</b> method with the <i>fFocus</i> parameter set to <b>FALSE</b> to release the keyboard focus without assigning it to any other object. In this case, the container must call the <a href="_win32_SetFocus_cpp">SetFocus</a> function with a <b>NULL</b> parameter so that no window has the focus.




## -see-also




<a href="https://msdn.microsoft.com/b077c256-1109-494c-95c2-2d33bccbe47b">IOleInPlaceActiveObject</a>



<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

