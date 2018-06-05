---
UID: NF:commctrl.Edit_SetCueBannerText
title: Edit_SetCueBannerText macro
author: windows-sdk-content
description: Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the EM_SETCUEBANNER message explicitly.
old-location: controls\Edit_SetCueBannerText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setcuebannertext.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Edit_SetCueBannerText, Edit_SetCueBannerText macro [Windows Controls], _win32_Edit_SetCueBannerText, _win32_Edit_SetCueBannerText_cpp, commctrl/Edit_SetCueBannerText, controls.Edit_SetCueBannerText, controls._win32_Edit_SetCueBannerText
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Edit_SetCueBannerText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Edit_SetCueBannerText macro


## -description


Sets the text that is displayed as the textual cue, or tip, for an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b">EM_SETCUEBANNER</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control. 


### -param lpcwText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a Unicode string that contains the text to set as the textual cue. 


## -remarks



An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue. When the user clicks the text, the text goes away and the user can type.

You cannot set a cue banner on a multiline edit control.

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b">EM_SETCUEBANNER</a>



<a href="https://msdn.microsoft.com/2a71b92c-f57a-4c27-80b7-e1d9092f3701">Edit Controls</a>



<b>Reference</b>
 

 

