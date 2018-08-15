---
UID: NF:mmc.IExtendTaskPad.EnumTasks
title: IExtendTaskPad::EnumTasks
author: windows-sdk-content
description: The IExtendTaskPad::EnumTasks method enables MMC to get a pointer to the IEnumTASK interface of the object that contains the snap-in's tasks.
old-location: mmc\iextendtaskpad_enumtasks.htm
old-project: MMC
ms.assetid: 5faced6f-68aa-453e-b5da-99b79e9c8e15
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnumTasks, EnumTasks method [MMC], EnumTasks method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],EnumTasks method, IExtendTaskPad.EnumTasks, IExtendTaskPad::EnumTasks, _slate_iextendtaskpad_enumtasks, mmc.iextendtaskpad_enumtasks, mmc/IExtendTaskPad::EnumTasks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendTaskPad.EnumTasks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendTaskPad::EnumTasks


## -description


The <b>IExtendTaskPad::EnumTasks</b> method enables MMC to get a pointer to the 
IEnumTASK interface of the object that contains the snap-in's tasks.


## -parameters




### -param pdo [in]

A pointer to the data object for the scope item that owns the taskpad.


### -param szTaskGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls <a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, szTaskGroup is a <b>NULL</b> string.


### -param ppEnumTASK [out]

A pointer to address of 
IEnumTASK interface of the object that contains the snap-in's tasks.


## -returns



This method can return one of these values.




## -remarks



MMC calls this method each time a taskpad from the snap-in is displayed. MMC also calls the method if the snap-in extends another snap-in's taskpad in order to get a pointer to the snap-in's 
IEnumTASK interface.




## -see-also




<a href="https://msdn.microsoft.com/7cf1ff4f-bd45-4ead-a005-e0f38aed9039">IEnumTASK</a>



<a href="https://msdn.microsoft.com/30f5b526-d2d5-48a6-be5f-d0f2ba9397c4">IExtendTaskPad</a>
 

 

