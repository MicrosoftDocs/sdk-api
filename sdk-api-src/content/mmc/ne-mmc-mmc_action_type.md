---
UID: NE:mmc._MMC_ACTION_TYPE
title: MMC_ACTION_TYPE (mmc.h)
description: The MMC_ACTION_TYPE enumeration is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_ACTION_ID","MMC_ACTION_LINK","MMC_ACTION_SCRIPT","MMC_ACTION_TYPE","MMC_ACTION_TYPE enumeration [MMC]","MMC_ACTION_UNINITIALIZED","_slate_mmc_action_type","mmc.mmc_action_type","mmc/MMC_ACTION_ID","mmc/MMC_ACTION_LINK","mmc/MMC_ACTION_SCRIPT","mmc/MMC_ACTION_TYPE","mmc/MMC_ACTION_UNINITIALIZED"]
old-location: mmc\mmc_action_type.htm
tech.root: mmc
ms.assetid: 08d9929a-ca55-4f71-8e9f-411e01e363d6
ms.date: 12/05/2018
ms.keywords: MMC_ACTION_ID, MMC_ACTION_LINK, MMC_ACTION_SCRIPT, MMC_ACTION_TYPE, MMC_ACTION_TYPE enumeration [MMC], MMC_ACTION_UNINITIALIZED, _slate_mmc_action_type, mmc.mmc_action_type, mmc/MMC_ACTION_ID, mmc/MMC_ACTION_LINK, mmc/MMC_ACTION_SCRIPT, mmc/MMC_ACTION_TYPE, mmc/MMC_ACTION_UNINITIALIZED
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
req.typenames: MMC_ACTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_ACTION_TYPE
 - mmc/_MMC_ACTION_TYPE
 - MMC_ACTION_TYPE
 - mmc/MMC_ACTION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_ACTION_TYPE
---

# MMC_ACTION_TYPE enumeration


## -description

The 
MMC_ACTION_TYPE enumeration is introduced in MMC 1.1.

The 
MMC_ACTION_TYPE enumeration defines the types of action that can be triggered when a user clicks a task on a taskpad. These values are used in the eActionType member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task">MMC_TASK</a> structure, which is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a> method.

## -enum-fields

### -field MMC_ACTION_UNINITIALIZED:-1

No actions specified.

### -field MMC_ACTION_ID

When the user clicks the task, MMC calls 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> and returns the command ID specified in the nCommandID member of the 
MMC_TASK structure that was filled in when MMC called <a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a> to add the task to the taskpad.

### -field MMC_ACTION_LINK

When the user clicks the task, MMC activates the link specified by the szActionURL member of the 
MMC_TASK structure.

### -field MMC_ACTION_SCRIPT

When the user clicks the task, MMC executes the script contained in the szScript member of 
MMC_TASK using the window.execScript method on the taskpad DHTML page.
