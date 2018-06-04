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

# CopyAcceleratorTableW function


## -description


Copies the specified accelerator table. This function is used to obtain the accelerator-table data that corresponds to an accelerator-table handle, or to determine the size of the accelerator-table data.


## -parameters




### -param hAccelSrc [in]

Type: <b>HACCEL</b>

A handle to the accelerator table to copy.


### -param lpAccelDst [out, optional]

Type: <b>LPACCEL</b>

An array of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures that receives the accelerator-table information.


### -param cAccelEntries [in]

Type: <b>int</b>

The number of <a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a> structures to copy to the buffer pointed to by the 
     <i>lpAccelDst</i> parameter.


## -returns



Type: <b>int</b>

If 
      <i>lpAccelDst</i> is <b>NULL</b>, the return value specifies the number of accelerator-table entries in the original table. Otherwise, it specifies the number of accelerator-table entries that were copied.




## -see-also




<a href="https://msdn.microsoft.com/9995bfc3-adc5-4a6d-b834-a96e1ceb6ea0">ACCEL</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0d8a970c-68b2-45e6-8702-2490029c1e1d">TranslateAccelerator</a>
 

 

