---
UID: NE:winuser.DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS
title: DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS (winuser.h)
description: Describes per-monitor DPI scaling behavior overrides for child windows within dialogs. The values in this enumeration are bitfields and can be combined.
helpviewer_keywords: ["DCDC_DEFAULT","DCDC_DISABLE_FONT_UPDATE","DCDC_DISABLE_RELAYOUT","DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR","DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR enumeration [High DPI]","DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS","DIALOG_SCALING_BEHAVIOR","DIALOG_SCALING_BEHAVIOR enumeration [High DPI]","hidpi.dialog_scaling_behavior","winuser/DCDC_DEFAULT","winuser/DCDC_DISABLE_FONT_UPDATE","winuser/DCDC_DISABLE_RELAYOUT","winuser/DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR"]
old-location: hidpi\dialog_scaling_behavior.htm
tech.root: hidpi
ms.assetid: B368D997-F409-491A-8578-004C7408A160
ms.date: 12/05/2018
ms.keywords: DCDC_DEFAULT, DCDC_DISABLE_FONT_UPDATE, DCDC_DISABLE_RELAYOUT, DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR, DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR enumeration [High DPI], DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS, DIALOG_SCALING_BEHAVIOR, DIALOG_SCALING_BEHAVIOR enumeration [High DPI], hidpi.dialog_scaling_behavior, winuser/DCDC_DEFAULT, winuser/DCDC_DISABLE_FONT_UPDATE, winuser/DCDC_DISABLE_RELAYOUT, winuser/DIALOG_CONTROL_DPI_CHANGE_BEHAVIOR
f1_keywords:
- winuser/DIALOG_SCALING_BEHAVIOR
dev_langs:
- c++
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- winuser.h
api_name:
- DIALOG_SCALING_BEHAVIOR
targetos: Windows
req.typenames: DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS
req.redist: 
ms.custom: 19H1
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



This enum is used with <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior">SetDialogControlDpiChangeBehavior</a> in order to override the default per-monitor DPI scaling behavior for a child window within a dialog.

These settings only apply to individual controls within dialogs. The dialog-wide per-monitor DPI scaling behavior of a dialog is controlled by <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors">DIALOG_DPI_CHANGE_BEHAVIORS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior">GetDialogControlDpiChangeBehavior</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior">SetDialogControlDpiChangeBehavior</a>
 

 

