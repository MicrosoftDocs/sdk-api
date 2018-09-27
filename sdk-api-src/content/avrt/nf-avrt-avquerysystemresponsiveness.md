---
UID: NF:avrt.AvQuerySystemResponsiveness
title: AvQuerySystemResponsiveness function
author: windows-sdk-content
description: Retrieves the system responsiveness setting used by the multimedia class scheduler service.
old-location: base\avquerysystemresponsiveness.htm
tech.root: procthread
ms.assetid: 87184232-9f58-4a59-87e9-fdd081a7dc5c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: AvQuerySystemResponsiveness, AvQuerySystemResponsiveness function, avrt/AvQuerySystemResponsiveness, base.avquerysystemresponsiveness
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvQuerySystemResponsiveness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AvQuerySystemResponsiveness function


## -description


Retrieves the system responsiveness setting used by the multimedia class scheduler service.


## -parameters




### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function.


### -param SystemResponsivenessValue [out]

The system responsiveness value. This value can range from 10 to 100 percent.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>
 

 

