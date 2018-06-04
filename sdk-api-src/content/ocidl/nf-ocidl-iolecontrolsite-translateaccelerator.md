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

# IOleControlSite::TranslateAccelerator


## -description


Passes a keystroke to the control site for processing.


## -parameters




### -param pMsg [in]

A pointer to the <a href="_win32_MSG_str_cpp">MSG</a> structure describing the keystroke to be processed.


### -param grfModifiers [in]

Flags describing the state of the Control, Alt, and Shift keys. The value of the flag can be any valid <a href="https://msdn.microsoft.com/5a85158d-33a7-4c99-a636-42f7c68dc3ce">KEYMODIFIERS</a> enumeration values.


## -returns



This method can return the following values.

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
The container processed the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The container did not process the message. This value must also be returned in all other error cases besides E_NOTIMPL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The container does not implement accelerator support.

</td>
</tr>
</table>
 




## -remarks



This method is called by a control that can be UI-active. In such cases, a control can process all keystrokes first through <a href="https://msdn.microsoft.com/ce460c52-c7aa-4ee4-955e-76407af7cf1e">IOleInPlaceActiveObject::TranslateAccelerator</a>, according to normal OLE Compound Document rules. Inside that method, the control can give the container certain messages to process first by calling <b>IOleControlSite::TranslateAccelerator</b> and using the return value to determine if any processing took place. Otherwise, the control always processes the message first. If the control does not use the keystroke as an accelerator, it passes the keystroke to the container through this method.




## -see-also




<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>



<a href="https://msdn.microsoft.com/ce460c52-c7aa-4ee4-955e-76407af7cf1e">IOleInPlaceActiveObject::TranslateAccelerator</a>
 

 

