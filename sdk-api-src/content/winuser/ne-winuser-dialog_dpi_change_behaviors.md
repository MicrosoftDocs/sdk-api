---
UID: NE:winuser.DIALOG_DPI_CHANGE_BEHAVIORS
title: DIALOG_DPI_CHANGE_BEHAVIORS (winuser.h)
author: windows-sdk-content
description: In Per Monitor v2 contexts, dialogs will automatically respond to DPI changes by resizing themselves and re-computing the positions of their child windows (here referred to as re-layouting).
old-location: hidpi\dialog_dpi_change_behaviors.htm
tech.root: hidpi
ms.assetid: 26248777-E95F-49BE-82D6-7237FAEE0627
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDC_DEFAULT, DDC_DISABLE_ALL, DDC_DISABLE_CONTROL_RELAYOUT, DDC_DISABLE_RESIZE, DIALOG_DPI_CHANGE_BEHAVIORS, DIALOG_DPI_CHANGE_BEHAVIORS enumeration [High DPI], hidpi.dialog_dpi_change_behaviors, winuser/DDC_DEFAULT, winuser/DDC_DISABLE_ALL, winuser/DDC_DISABLE_CONTROL_RELAYOUT, winuser/DDC_DISABLE_RESIZE, winuser/DIALOG_DPI_CHANGE_BEHAVIORS
ms.topic: enum
f1_keywords: 
 - "winuser/DIALOG_DPI_CHANGE_BEHAVIORS"
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
 - DIALOG_DPI_CHANGE_BEHAVIORS
targetos: Windows
req.typenames: DIALOG_DPI_CHANGE_BEHAVIORS
req.redist: 
ms.custom: 19H1
---

# DIALOG_DPI_CHANGE_BEHAVIORS enumeration


## -description


In <a href="https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context">Per Monitor v2 contexts</a>, dialogs will automatically respond to DPI changes by resizing themselves and re-computing the positions of their child windows (here referred to as re-layouting). This enum works in conjunction with <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior">SetDialogDpiChangeBehavior</a> in order to override the default DPI scaling behavior for dialogs.

This does not affect DPI scaling behavior for the child windows of dialogs (beyond re-layouting), which is controlled by <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>.


## -enum-fields




### -field DDC_DEFAULT

The default behavior of the dialog manager. In response to a DPI change, the dialog manager will re-layout each control, update the font on each control, resize the dialog, and update the dialog's own font.


### -field DDC_DISABLE_ALL

Prevents the dialog manager from responding to <a href="https://docs.microsoft.com/windows/desktop/hidpi/wm-getdpiscaledsize">WM_GETDPISCALEDSIZE</a> and <a href="https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged">WM_DPICHANGED</a>, disabling all default DPI scaling behavior.


### -field DDC_DISABLE_RESIZE

Prevents the dialog manager from resizing the dialog in response to a DPI change.


### -field DDC_DISABLE_CONTROL_RELAYOUT

Prevents the dialog manager from re-layouting all of the dialogue's immediate children HWNDs in response to a DPI change.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior">GetDialogDpiChangeBehavior</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior">SetDialogDpiChangeBehavior</a>
 

 

