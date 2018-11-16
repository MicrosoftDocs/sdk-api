---
UID: NF:commctrl.Button_GetNoteLength
title: Button_GetNoteLength macro
author: windows-sdk-content
description: Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the BCM_GETNOTELENGTH message explicitly.
old-location: controls\Button_GetNoteLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getnotelength.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
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
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- Button_GetNoteLength
: 
---

# Button_GetNoteLength macro


## -description


Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the <a href="https://msdn.microsoft.com/62385485-b553-47e9-9f15-696cc4694752">BCM_GETNOTELENGTH</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


## -remarks



Beginning with comctl32 DLL version 6.01, command link buttons may have a note. For information on DLL versions, see <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Common Control Versions</a>.

The <b>Button_GetNoteLength</b> macro works only with the <a href="Button_Styles.htm">BS_COMMANDLINK</a> and <a href="Button_Styles.htm">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/30254cb5-43cd-407f-8ad6-bd7f9ec3edc7">Button Styles</a>



<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

