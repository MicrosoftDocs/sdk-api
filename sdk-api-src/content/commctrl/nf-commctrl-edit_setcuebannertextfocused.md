---
UID: NF:commctrl.Edit_SetCueBannerTextFocused
title: Edit_SetCueBannerTextFocused macro
author: windows-sdk-content
description: Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the EM_SETCUEBANNER message explicitly.
old-location: controls\Edit_SetCueBannerTextFocused.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setcuebannertextfocused.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Edit_SetCueBannerTextFocused, Edit_SetCueBannerTextFocused macro [Windows Controls], _shell_Edit_SetCueBannerTextFocused, _shell_Edit_SetCueBannerTextFocused_cpp, commctrl/Edit_SetCueBannerTextFocused, controls.Edit_SetCueBannerTextFocused, controls._shell_Edit_SetCueBannerTextFocused
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
 - Edit_SetCueBannerTextFocused
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
- Edit_SetCueBannerTextFocused
: 
---

# Edit_SetCueBannerTextFocused macro


## -description


Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b">EM_SETCUEBANNER</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control.


### -param lpcwText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a Unicode string that contains the text to set as the textual cue.


### -param fDrawFocused

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Sets whether the cue text is drawn when the control has keyboard focus.


## -remarks



An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue. <i>fDrawFocused</i> controls when the cue text disappears. If <i>fDrawFocused</i> is <b>FALSE</b>, then the cue text disappears when the edit control receives focus. If <i>fDrawFocused</i> is <b>TRUE</b>, then the cue text disappears when the user enters text into the edit control.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b">EM_SETCUEBANNER</a>



<a href="https://msdn.microsoft.com/2a71b92c-f57a-4c27-80b7-e1d9092f3701">Edit Controls</a>



<a href="https://msdn.microsoft.com/7094c38f-9e30-49e2-b830-1007a7a9dc97">Edit_SetCueBannerText</a>



<b>Reference</b>
 

 

