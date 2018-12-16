---
UID: NE:mmc._MMC_ACTION_TYPE
title: MMC_ACTION_TYPE
author: windows-sdk-content
description: The MMC_ACTION_TYPE enumeration is introduced in MMC 1.1.
old-location: mmc\mmc_action_type.htm
tech.root: mmc
ms.assetid: 08d9929a-ca55-4f71-8e9f-411e01e363d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MMC_ACTION_ID, MMC_ACTION_LINK, MMC_ACTION_SCRIPT, MMC_ACTION_TYPE, MMC_ACTION_TYPE enumeration [MMC], MMC_ACTION_UNINITIALIZED, _slate_mmc_action_type, mmc.mmc_action_type, mmc/MMC_ACTION_ID, mmc/MMC_ACTION_LINK, mmc/MMC_ACTION_SCRIPT, mmc/MMC_ACTION_TYPE, mmc/MMC_ACTION_UNINITIALIZED
ms.topic: enum
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
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_ACTION_TYPE
product: Windows
targetos: Windows
req.typenames: MMC_ACTION_TYPE
req.redist: 
---

# MMC_ACTION_TYPE enumeration


## -description


The 
MMC_ACTION_TYPE enumeration is introduced in MMC 1.1.

The 
MMC_ACTION_TYPE enumeration defines the types of action that can be triggered when a user clicks a task on a taskpad. These values are used in the eActionType member of the 
<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a> structure, which is filled in by the 
<a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a> method.


## -enum-fields




### -field MMC_ACTION_UNINITIALIZED

No actions specified.


### -field MMC_ACTION_ID

When the user clicks the task, MMC calls 
<a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">IExtendTaskPad::TaskNotify</a> and returns the command ID specified in the nCommandID member of the 
MMC_TASK structure that was filled in when MMC called <a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a> to add the task to the taskpad.


### -field MMC_ACTION_LINK

When the user clicks the task, MMC activates the link specified by the szActionURL member of the 
MMC_TASK structure.


### -field MMC_ACTION_SCRIPT

When the user clicks the task, MMC executes the script contained in the szScript member of 
MMC_TASK using the window.execScript method on the taskpad DHTML page.

