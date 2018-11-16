---
UID: NF:mmc.IEnumTASK.Next
title: IEnumTASK::Next
author: windows-sdk-content
description: The IEnumTASK::Next method enables MMC to retrieve the next task in the snap-in's list of tasks.
old-location: mmc\ienumtask_next.htm
tech.root: MMC
ms.assetid: cb568307-7172-4941-a888-ff059f5256b6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumTASK interface [MMC],Next method, IEnumTASK.Next, IEnumTASK::Next, Next, Next method [MMC], Next method [MMC],IEnumTASK interface, _slate_ienumtask_next, mmc.ienumtask_next, mmc/IEnumTASK::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - COM
api_location:
 - Mmc.h
api_name:
 - IEnumTASK.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IEnumTASK.Next
: 
---

# IEnumTASK::Next


## -description


The <b>IEnumTASK::Next</b> method enables MMC to retrieve the next task in the snap-in's list of tasks.


## -parameters




### -param celt [in]

A value that specifies the number of tasks to provide. MMC always enumerates tasks one at a time; therefore, celt is always 1.


### -param rgelt [out]

A pointer to an 
<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a> structure that the snap-in fills in to represent the task to add to the taskpad. Be aware that the caller (MMC) allocates the memory for the structure.


### -param pceltFetched [out]

A pointer to a value that specifies the number of tasks returned. If the snap-in successfully returned one or more tasks, set the value to the number of tasks that were successfully returned. Because MMC always requests one task at a time (celt is always 1), pceltFetched should be set to 1 if the task was successfully returned. If the snap-in has no more tasks in its list, or if the snap-in fails to fill in the 
MMC_TASK structure, set the value to 0.


## -returns



This method can return one of these values.




## -remarks



MMC calls this method to enumerate the list of tasks that the snap-in must add to the taskpad. MMC calls this method until it returns S_FALSE to indicate there are no more tasks for the snap-in to add to the taskpad.




## -see-also




<a href="https://msdn.microsoft.com/30f5b526-d2d5-48a6-be5f-d0f2ba9397c4">IExtendTaskPad</a>



<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a>



<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a>



<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a>



<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a>
 

 

