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

# IFECommon::SetDefaultIME


## -description


Allows the Microsoft IME to become the default IME in the keyboard layout.

This method only applies when Microsoft IME uses the Input Method Manager (IMM) of the operating system.


## -parameters






## -returns



<ul>
<li><b>S_OK</b> if successful.</li>
<li><b>IFEC_S_ALREADY_DEFAULT</b> if this Microsoft IME is already the default IME.</li>
<li>Otherwise <b>E_FAIL</b>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9FBECA6F-F162-485D-938F-FADC2D47083E">IFECommon</a>
 

 

