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

# SetupGetNonInteractiveMode function


## -description


The <b>SetupGetNonInteractiveMode</b> function returns the value of a SetupAPI non-interactive flag  that indicates whether the caller's process can interact with a user through user interface components, such as dialog boxes. 


## -parameters






## -returns



<b>SetupGetNonInteractiveMode</b> returns <b>TRUE</b> if the caller's process cannot display interactive user interface elements, such as dialog boxes. Otherwise, the function returns <b>FALSE</b>, which indicates that the process can display interactive user interface elements. 




## -remarks



Installation applications and <a href="devinst.writing_a_co_installer">co-installers</a> can use this function to determine whether the current process can display interactive user interface elements such as dialog boxes. <a href="devinst.setupapi">SetupAPI</a> runs a class installer or a co-installer either in an interactive or in a non-interactive process, depending on which <a href="devinst.handling_dif_codes">DIF code</a> SetupAPI is processing.

An installation application can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552213">SetupSetNonInteractiveMode</a> to set the SetupAPI non-interactive flag that controls whether SetupAPI can display interactive user interface elements in the caller's context. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552213">SetupSetNonInteractiveMode</a>
 

 

