---
UID: NS:ocidl.tagCONTROLINFO
title: tagCONTROLINFO
author: windows-sdk-content
description: Contains parameters that describe a control's keyboard mnemonics and keyboard behavior. The structure is populated during the IOleControl::GetControlInfo method.
old-location: com\controlinfo.htm
tech.root: com
ms.assetid: 3f22dc1d-554a-4dd1-a79a-121117f65caf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPCONTROLINFO, CONTROLINFO, CONTROLINFO structure [COM], LPCONTROLINFO, LPCONTROLINFO structure pointer [COM], _ctrl_CONTROLINFO, com.controlinfo, ocidl/CONTROLINFO, ocidl/LPCONTROLINFO, tagCONTROLINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - CONTROLINFO
product: Windows
targetos: Windows
req.typenames: CONTROLINFO, *LPCONTROLINFO
req.redist: 
---

# tagCONTROLINFO structure


## -description


Contains parameters that describe a control's keyboard mnemonics and keyboard behavior. The structure is populated during the <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a> method.



## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field hAccel

A handle to an array of <a href="https://msdn.microsoft.com/en-us/library/ms646340(v=VS.85).aspx">ACCEL</a> structures, each structure describing a keyboard mnemonic. The array is created with the <a href="https://msdn.microsoft.com/en-us/library/ms646365(v=VS.85).aspx">CreateAcceleratorTable</a> function. The control always maintains the memory for this array; the caller of <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a> should not attempt to free the memory.


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
 

 

