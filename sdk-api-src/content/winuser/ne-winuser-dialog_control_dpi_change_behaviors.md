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

# DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS enumeration


## -description


Describes per-monitor DPI scaling behavior overrides for child windows within dialogs. The values in this enumeration are bitfields and can be combined.


## -enum-fields




### -field DCDC_DEFAULT

The default behavior of the dialog manager. The dialog managed will update the font, size, and position of the child window on DPI changes.


### -field DCDC_DISABLE_FONT_UPDATE

Prevents the dialog manager from sending an updated font to the child window via WM_SETFONT in response to a DPI change.


### -field DCDC_DISABLE_RELAYOUT

Prevents the dialog manager from resizing and repositioning  the child window in response to a DPI change.


## -remarks



This enum is used with <a href="https://msdn.microsoft.com/52BB557B-0D70-4189-9BD0-EB94188EA4E7">SetDialogControlDpiChangeBehavior</a> in order to override the default per-monitor DPI scaling behavior for a child window within a dialog.

These settings only apply to individual controls within dialogs. The dialog-wide per-monitor DPI scaling behavior of a dialog is controlled by <a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a>.




## -see-also




<a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/1651353F-5823-41B8-AE52-016AEBA6C4F0">GetDialogControlDpiChangeBehavior</a>



<a href="https://msdn.microsoft.com/52BB557B-0D70-4189-9BD0-EB94188EA4E7">SetDialogControlDpiChangeBehavior</a>
 

 

