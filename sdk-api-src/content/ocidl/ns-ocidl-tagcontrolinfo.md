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

# tagCONTROLINFO structure


## -description


Contains parameters that describe a control's keyboard mnemonics and keyboard behavior. The structure is populated during the <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a> method.



## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field hAccel

A handle to an array of <a href="_win32_ACCEL_str_cpp">ACCEL</a> structures, each structure describing a keyboard mnemonic. The array is created with the <a href="_win32_CreateAcceleratorTable_cpp">CreateAcceleratorTable</a> function. The control always maintains the memory for this array; the caller of <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a> should not attempt to free the memory.


### -field cAccel

The number of mnemonics described in the <b>hAccel</b> field. This value can be zero to indicate no mnemonics.


### -field dwFlags

Flags that indicate the keyboard behavior of the control. The possible values are:

<ul>
<li>CTRLINFO_EATS_RETURN: When the control has the focus, it will process the Return key. 
</li>
<li>CTRLINFO_EATS_ESCAPE: When the control has the focus, it will process the Escape key. </li>
</ul>
When the control has the focus, the dialog box containing the control cannot use the Return or Escape keys as mnemonics for the default and cancel buttons.


## -see-also




<a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a>
 

 

