---
UID: NF:mmc.IExtendTaskPad.EnumTasks
title: IExtendTaskPad::EnumTasks (mmc.h)
description: The IExtendTaskPad::EnumTasks method enables MMC to get a pointer to the IEnumTASK interface of the object that contains the snap-in's tasks.
helpviewer_keywords: ["EnumTasks","EnumTasks method [MMC]","EnumTasks method [MMC]","IExtendTaskPad interface","IExtendTaskPad interface [MMC]","EnumTasks method","IExtendTaskPad.EnumTasks","IExtendTaskPad::EnumTasks","_slate_iextendtaskpad_enumtasks","mmc.iextendtaskpad_enumtasks","mmc/IExtendTaskPad::EnumTasks"]
old-location: mmc\iextendtaskpad_enumtasks.htm
tech.root: mmc
ms.assetid: 5faced6f-68aa-453e-b5da-99b79e9c8e15
ms.date: 12/05/2018
ms.keywords: EnumTasks, EnumTasks method [MMC], EnumTasks method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],EnumTasks method, IExtendTaskPad.EnumTasks, IExtendTaskPad::EnumTasks, _slate_iextendtaskpad_enumtasks, mmc.iextendtaskpad_enumtasks, mmc/IExtendTaskPad::EnumTasks
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtendTaskPad::EnumTasks
 - mmc/IExtendTaskPad::EnumTasks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendTaskPad.EnumTasks
---

# IExtendTaskPad::EnumTasks


## -description

The <b>IExtendTaskPad::EnumTasks</b> method enables MMC to get a pointer to the 
IEnumTASK interface of the object that contains the snap-in's tasks.

## -parameters

### -param pdo [in]

A pointer to the data object for the scope item that owns the taskpad.

### -param szTaskGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, szTaskGroup is a <b>NULL</b> string.

### -param ppEnumTASK [out]

A pointer to address of 
IEnumTASK interface of the object that contains the snap-in's tasks.

## -returns

This method can return one of these values.

## -remarks

MMC calls this method each time a taskpad from the snap-in is displayed. MMC also calls the method if the snap-in extends another snap-in's taskpad in order to get a pointer to the snap-in's 
IEnumTASK interface.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ienumtask">IEnumTASK</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a>