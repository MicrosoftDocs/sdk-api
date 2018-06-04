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

# IsAccelerator function


## -description


Determines whether the specified keystroke maps to an accelerator in the specified accelerator table.


## -parameters




### -param hAccel [in]

A handle to the accelerator table.


### -param cAccelEntries [in]

The number of entries in the accelerator table.


### -param lpMsg [in]

A pointer to the keystroke message to be translated.


### -param lpwCmd [out]

A pointer to a variable  to receive the corresponding command identifier if there is an accelerator for the keystroke. This parameter may be <b>NULL</b>.


## -returns



If the message is for the object application, the return value is <b>TRUE</b>. If the message is not for the object and should be forwarded to the container, the return value is <b>FALSE</b>.




## -remarks



While an object is active in-place, the object always has first chance to translate the keystrokes into accelerators. If the keystroke corresponds to one of its accelerators, the object must not call the <a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a> function â€” even if its call to the <a href="_win32_TranslateAccelerator_cpp">TranslateAccelerator</a> function fails. Failure to process keystrokes in this manner can lead to inconsistent behavior.

If the keystroke is not one of the object's accelerators, then the object must call <a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a> to let the container try its accelerator translation.

The object's server can call <b>IsAccelerator</b> to determine if the accelerator message belongs to it. Some servers do accelerator translation on their own and do not call <a href="_win32_TranslateAccelerator_cpp">TranslateAccelerator</a>. Those applications will not call <b>IsAccelerator</b>, because they already have the information.





## -see-also




<a href="https://msdn.microsoft.com/c590efef-7f03-4ae6-a35f-eff2fc4da3d9">OleTranslateAccelerator</a>



<a href="_win32_TranslateAccelerator_cpp">TranslateAccelerator</a>
 

 

