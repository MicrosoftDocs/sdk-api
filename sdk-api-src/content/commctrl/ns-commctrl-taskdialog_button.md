---
UID: NS:commctrl._TASKDIALOG_BUTTON
title: TASKDIALOG_BUTTON (commctrl.h)
description: The TASKDIALOG_BUTTON structure contains information used to display a button in a task dialog. The TASKDIALOGCONFIG structure uses this structure.
helpviewer_keywords: ["TASKDIALOG_BUTTON","TASKDIALOG_BUTTON structure [Windows Controls]","_shell_TASKDIALOG_BUTTON","_shell_TASKDIALOG_BUTTON_cpp","commctrl/TASKDIALOG_BUTTON","controls.TASKDIALOG_BUTTON","controls._shell_TASKDIALOG_BUTTON"]
old-location: controls\TASKDIALOG_BUTTON.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\taskdialogs\taskdialogreference\taskdialogstructures\taskdialog_button.htm
ms.date: 12/05/2018
ms.keywords: TASKDIALOG_BUTTON, TASKDIALOG_BUTTON structure [Windows Controls], _shell_TASKDIALOG_BUTTON, _shell_TASKDIALOG_BUTTON_cpp, commctrl/TASKDIALOG_BUTTON, controls.TASKDIALOG_BUTTON, controls._shell_TASKDIALOG_BUTTON
req.header: commctrl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TASKDIALOG_BUTTON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASKDIALOG_BUTTON
 - commctrl/_TASKDIALOG_BUTTON
 - TASKDIALOG_BUTTON
 - commctrl/TASKDIALOG_BUTTON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TASKDIALOG_BUTTON
---

# TASKDIALOG_BUTTON structure


## -description

The <b>TASKDIALOG_BUTTON</b> structure contains information used to display a button in a task dialog. The <a href="/windows/desktop/api/commctrl/ns-commctrl-taskdialogconfig">TASKDIALOGCONFIG</a> structure uses this structure.

## -struct-fields

### -field nButtonID

Type: <b>int</b>

Indicates the value to be returned when this button is selected.

### -field pszButtonText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

Pointer that references the string to be used to label the button. This parameter can be either a null-terminated string or an integer resource identifier passed to the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. When using Command Links, you delineate the command from the note by placing a new line character in the string.