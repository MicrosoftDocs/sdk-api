---
UID: NF:commctrl.Button_GetNoteLength
title: Button_GetNoteLength macro
author: windows-sdk-content
description: Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the BCM_GETNOTELENGTH message explicitly.
old-location: controls\Button_GetNoteLength.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getnotelength.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: Button_GetNoteLength, Button_GetNoteLength macro [Windows Controls], _shell_Button_GetNoteLength, _shell_Button_GetNoteLength_cpp, commctrl/Button_GetNoteLength, controls.Button_GetNoteLength, controls._shell_Button_GetNoteLength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Button_GetNoteLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_GetNoteLength macro


## -description


Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775967(v=VS.85).aspx">BCM_GETNOTELENGTH</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the button control.


## -remarks



Beginning with comctl32 DLL version 6.01, command link buttons may have a note. For information on DLL versions, see <a href="https://msdn.microsoft.com/en-us/library/Hh298349(v=VS.85).aspx">Common Control Versions</a>.

The <b>Button_GetNoteLength</b> macro works only with the <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_COMMANDLINK</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">Button Styles</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775947(v=VS.85).aspx">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

