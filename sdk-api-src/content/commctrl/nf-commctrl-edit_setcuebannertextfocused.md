---
UID: NF:commctrl.Edit_SetCueBannerTextFocused
title: Edit_SetCueBannerTextFocused macro (commctrl.h)
description: Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the EM_SETCUEBANNER message explicitly.
old-location: controls\Edit_SetCueBannerTextFocused.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setcuebannertextfocused.htm
ms.date: 12/05/2018
ms.keywords: Edit_SetCueBannerTextFocused, Edit_SetCueBannerTextFocused macro [Windows Controls], _shell_Edit_SetCueBannerTextFocused, _shell_Edit_SetCueBannerTextFocused_cpp, commctrl/Edit_SetCueBannerTextFocused, controls.Edit_SetCueBannerTextFocused, controls._shell_Edit_SetCueBannerTextFocused
f1_keywords:
- commctrl/Edit_SetCueBannerTextFocused
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetCueBannerTextFocused macro


## -description


Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setcuebanner">EM_SETCUEBANNER</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.


### -param lpcwText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A pointer to a Unicode string that contains the text to set as the textual cue.


### -param fDrawFocused

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Sets whether the cue text is drawn when the control has keyboard focus.


## -remarks



An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue. <i>fDrawFocused</i> controls when the cue text disappears. If <i>fDrawFocused</i> is <b>FALSE</b>, then the cue text disappears when the edit control receives focus. If <i>fDrawFocused</i> is <b>TRUE</b>, then the cue text disappears when the user enters text into the edit control.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/em-setcuebanner">EM_SETCUEBANNER</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/edit-controls">Edit Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-edit_setcuebannertext">Edit_SetCueBannerText</a>



<b>Reference</b>
 

 

