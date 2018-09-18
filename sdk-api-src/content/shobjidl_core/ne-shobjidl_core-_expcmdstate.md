---
UID: NE:shobjidl_core._EXPCMDSTATE
title: "_EXPCMDSTATE"
author: windows-sdk-content
description: EXPCMDSTATE values represent the command state of a Shell item.
old-location: shell\EXPCMDSTATE.htm
tech.root: shell
ms.assetid: 41e76b6e-9294-40b3-bb8b-bbfe487fd023
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ECS_CHECKBOX, ECS_CHECKED, ECS_DISABLED, ECS_ENABLED, ECS_HIDDEN, ECS_RADIOCHECK, EXPCMDSTATE, EXPCMDSTATE enumeration [Windows Shell], _EXPCMDSTATE, _shell_EXPCMDSTATE, shell.EXPCMDSTATE, shobjidl_core/ECS_CHECKBOX, shobjidl_core/ECS_CHECKED, shobjidl_core/ECS_DISABLED, shobjidl_core/ECS_ENABLED, shobjidl_core/ECS_HIDDEN, shobjidl_core/ECS_RADIOCHECK, shobjidl_core/EXPCMDSTATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - EXPCMDSTATE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _EXPCMDSTATE enumeration


## -description


<b>EXPCMDSTATE</b> values represent the command state of a Shell item.


## -enum-fields




### -field ECS_ENABLED

The item is enabled.


### -field ECS_DISABLED

The item is unavailable. It might be displayed to the user as a dimmed, inaccessible item.


### -field ECS_HIDDEN

The item is hidden.


### -field ECS_CHECKBOX

The item is displayed with a check box and that check box is not checked.


### -field ECS_CHECKED

The item is displayed with a check box and that check box is checked. <b>ECS_CHECKED</b> is always returned with ECS_CHECKBOX.


### -field ECS_RADIOCHECK

<b>Windows 7 and later</b>. The item is one of a group of mutually exclusive options selected through a radio button. ECS_RADIOCHECK does not imply that the item is the selected option, though it might be.


## -see-also




<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">IExplorerCommand::GetState</a>



<a href="https://msdn.microsoft.com/a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7">IExplorerCommandState::GetState</a>
 

 

