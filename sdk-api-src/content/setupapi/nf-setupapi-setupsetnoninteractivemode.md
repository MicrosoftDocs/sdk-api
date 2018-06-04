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

# SetupSetNonInteractiveMode function


## -description


The <b>SetupSetNonInteractiveMode</b> function sets a non-interactive SetupAPI flag that determines whether SetupAPI can interact with a user in the caller's context. 


## -parameters




### -param NonInteractiveFlag [in]

The Boolean value of the non-interactive flag. If <i>NonInteractive</i> is set to <b>TRUE</b>, SetupAPI runs in a non-interactive user mode and if <i>NonInteractive</i> is set to <b>FALSE</b>, SetupAPI runs in an interactive user mode.


## -returns



<b>SetupSetNonInteractiveMode</b> returns the previous setting of the non-interactive flag.




## -remarks



Installation applications and <a href="devinst.writing_a_co_installer">co-installers</a> can use this function to control whether SetupAPI can display interactive user interface elements, such as dialog boxes, in the caller's context. 

An installation application or an installer can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552207">SetupGetNonInteractiveMode</a> to retrieve the current value of the non-interactive flag. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552207">SetupGetNonInteractiveMode</a>
 

 

