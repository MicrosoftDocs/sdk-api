---
UID: NF:commctrl.Button_GetNote
title: Button_GetNote macro (commctrl.h)
description: Gets the text of the note associated with a command link button. You can use this macro or send the BCM_GETNOTE message explicitly.helpviewer_keywords: ["Button_GetNote","Button_GetNote macro [Windows Controls]","_shell_Button_GetNote","_shell_Button_GetNote_cpp","commctrl/Button_GetNote","controls.Button_GetNote","controls._shell_Button_GetNote"]
old-location: controls\Button_GetNote.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getnote.htm
ms.date: 12/05/2018
ms.keywords: Button_GetNote, Button_GetNote macro [Windows Controls], _shell_Button_GetNote, _shell_Button_GetNote_cpp, commctrl/Button_GetNote, controls.Button_GetNote, controls._shell_Button_GetNote
f1_keywords:
- commctrl/Button_GetNote
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Commctrl.h
api_name:
- Button_GetNote
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_GetNote macro


## -description


Gets the text of the note associated with a command link button. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-getnote">BCM_GETNOTE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.


### -param psz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A pointer to a null-terminated, Unicode string that contains the note.


### -param pcc

Type: <b>int</b>

A pointer to the length of the note, in characters.


## -remarks



This macro works only with the <a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">BS_COMMANDLINK</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">Button Styles</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/button-types-and-styles">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

