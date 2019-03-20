---
UID: NF:commctrl.Button_GetNote
title: Button_GetNote macro (commctrl.h)
author: windows-sdk-content
description: Gets the text of the note associated with a command link button. You can use this macro or send the BCM_GETNOTE message explicitly.
old-location: controls\Button_GetNote.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getnote.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Button_GetNote, Button_GetNote macro [Windows Controls], _shell_Button_GetNote, _shell_Button_GetNote_cpp, commctrl/Button_GetNote, controls.Button_GetNote, controls._shell_Button_GetNote
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_GetNote macro


## -description


Gets the text of the note associated with a command link button. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775965(v=VS.85).aspx">BCM_GETNOTE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param psz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a null-terminated, Unicode string that contains the note.


### -param pcc

Type: <b>int</b>

A pointer to the length of the note, in characters.


## -remarks



This macro works only with the <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_COMMANDLINK</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">Button Styles</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775947(v=VS.85).aspx">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

