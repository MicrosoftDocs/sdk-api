---
UID: NF:commctrl.Button_SetNote
title: Button_SetNote macro
author: windows-driver-content
description: Sets the text of the note associated with a specified command link button. You can use this macro or send the BCM_SETNOTE message explicitly.
old-location: controls\Button_SetNote.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setnote.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Button_SetNote, Button_SetNote macro [Windows Controls], _shell_Button_SetNote, _shell_Button_SetNote_cpp, commctrl/Button_SetNote, controls.Button_SetNote, controls._shell_Button_SetNote
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Button_SetNote
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_SetNote macro


## -description


Sets the text of the note associated with a specified command link button. You can use this macro or send the <a href="https://msdn.microsoft.com/c167072a-8207-4744-ac66-247141d726ab">BCM_SETNOTE</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param psz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PCWSTR</a></b>

A pointer to a null-terminated <b>WCHAR</b> string that contains the note.


## -remarks



Beginning with comctl32 DLL version 6.01, command link buttons may have a note.

This macro works only with the <a href="Button_Styles.htm">BS_COMMANDLINK</a> and <a href="Button_Styles.htm">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/30254cb5-43cd-407f-8ad6-bd7f9ec3edc7">Button Styles</a>



<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

