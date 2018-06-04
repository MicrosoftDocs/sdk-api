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

# CreateAcceleratorTableA function


## -description


Creates an accelerator table.


## -parameters




### -param paccel

TBD


### -param cAccel

TBD




#### - cEntries [in]

Type: <b>int</b>

The number of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures in the array. This must be within the range 1 to 32767 or the function will fail.


#### - lpaccl [in]

Type: <b>LPACCEL</b>

An array of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures that describes the accelerator table.


## -returns



Type: <b>HACCEL</b>

If the function succeeds, the return value is the handle to the created accelerator table; otherwise, it is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Before an application closes, it can use the <a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a> function to destroy any accelerator tables that it created by using the <b>CreateAcceleratorTable</b> function.


#### Examples

For an example, see <a href="using_keyboard_accelerators.htm">Creating User Editable Accelerators</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/9dd87782-aa38-44eb-a35d-3d990cece223">CopyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>
 

 

