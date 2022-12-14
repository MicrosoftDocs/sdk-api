---
UID: NE:uiribbon.UI_EXECUTIONVERB
title: UI_EXECUTIONVERB (uiribbon.h)
description: Specifies values that identify the execution IDs that map to actions a user can initiate on a Command.
helpviewer_keywords: ["UI_EXECUTIONVERB","UI_EXECUTIONVERB enumeration [Windows Ribbon]","UI_EXECUTIONVERB_CANCELPREVIEW","UI_EXECUTIONVERB_EXECUTE","UI_EXECUTIONVERB_PREVIEW","scenicintent_UI_EXECUTIONVERB","uiribbon/UI_EXECUTIONVERB","uiribbon/UI_EXECUTIONVERB_CANCELPREVIEW","uiribbon/UI_EXECUTIONVERB_EXECUTE","uiribbon/UI_EXECUTIONVERB_PREVIEW","windowsribbon.windowsribbon_ui_executionverb"]
old-location: windowsribbon\windowsribbon_ui_executionverb.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_executionverb.htm
ms.date: 12/05/2018
ms.keywords: UI_EXECUTIONVERB, UI_EXECUTIONVERB enumeration [Windows Ribbon], UI_EXECUTIONVERB_CANCELPREVIEW, UI_EXECUTIONVERB_EXECUTE, UI_EXECUTIONVERB_PREVIEW, scenicintent_UI_EXECUTIONVERB, uiribbon/UI_EXECUTIONVERB, uiribbon/UI_EXECUTIONVERB_CANCELPREVIEW, uiribbon/UI_EXECUTIONVERB_EXECUTE, uiribbon/UI_EXECUTIONVERB_PREVIEW, windowsribbon.windowsribbon_ui_executionverb
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_EXECUTIONVERB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_EXECUTIONVERB
 - uiribbon/UI_EXECUTIONVERB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_EXECUTIONVERB
---

# UI_EXECUTIONVERB enumeration


## -description

Specifies values that identify the execution IDs that map to actions a user can initiate on a <a href="/windows/desktop/windowsribbon/windowsribbon-element-command">Command</a>.

## -enum-fields

### -field UI_EXECUTIONVERB_EXECUTE:0

Execute a command.

### -field UI_EXECUTIONVERB_PREVIEW:1

Show a preview of a visual element.

### -field UI_EXECUTIONVERB_CANCELPREVIEW:2

Cancel a preview of a visual element.

## -remarks

In the Ribbon framework, user actions are called executions. 

For example, if a user hovers the mouse over a gallery item,  UI_EXECUTIONVERB_PREVIEW is passed in a call to the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute">IUICommandHandler::Execute</a> function of the gallery to indicate that  a live preview event occurred on the item.  If the user clicks the gallery item, UI_EXECUTIONVERB_EXECUTE is passed in a subsequent call to the <b>IUICommandHandler::Execute</b> function to indicate that the item was executed.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-commandscontrols">Understanding Commands and Controls</a>



<a href="/windows/desktop/windowsribbon/ribbon-controls-galleries">Working with Galleries</a>
