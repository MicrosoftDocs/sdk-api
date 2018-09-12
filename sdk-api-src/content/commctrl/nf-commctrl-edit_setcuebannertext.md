---
UID: NF:commctrl.Edit_SetCueBannerText
title: Edit_SetCueBannerText macro
author: windows-sdk-content
description: Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the EM_SETCUEBANNER message explicitly.
old-location: controls\Edit_SetCueBannerText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setcuebannertext.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Edit_SetCueBannerText, Edit_SetCueBannerText macro [Windows Controls], _win32_Edit_SetCueBannerText, _win32_Edit_SetCueBannerText_cpp, commctrl/Edit_SetCueBannerText, controls.Edit_SetCueBannerText, controls._win32_Edit_SetCueBannerText
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
 - Edit_SetCueBannerText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetCueBannerText macro


## -description


Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761639(v=VS.85).aspx">EM_SETCUEBANNER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the edit control. 


### -param lpcwText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCWSTR</a></b>

A pointer to a Unicode string that contains the text to set as the textual cue. 


## -remarks



An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue. When the user clicks the text, the text goes away and the user can type.

You cannot set a cue banner on a multiline edit control.

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb761639(v=VS.85).aspx">EM_SETCUEBANNER</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775458(v=VS.85).aspx">Edit Controls</a>



<b>Reference</b>
 

 

