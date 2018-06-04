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

# DestroyAcceleratorTable function


## -description


Destroys an accelerator table.


## -parameters




### -param hAccel [in]

Type: <b>HACCEL</b>

A handle to the accelerator table to be destroyed. This handle must have been created by a call to the <a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a> or <a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. However, if the table has been loaded more than one call to <a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>, the function will return a nonzero value only when <b>DestroyAcceleratorTable</b> has been called an equal number of times.

If the function fails, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9dd87782-aa38-44eb-a35d-3d990cece223">CopyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>
 

 

