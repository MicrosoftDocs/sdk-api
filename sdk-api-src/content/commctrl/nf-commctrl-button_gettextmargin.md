---
UID: NF:commctrl.Button_GetTextMargin
title: Button_GetTextMargin macro
author: windows-sdk-content
description: Gets the margins used to draw text in a button control. You can use this macro or send the BCM_GETTEXTMARGIN message explicitly.
old-location: controls\Button_GetTextMargin.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_gettextmargin.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Button_GetTextMargin, Button_GetTextMargin macro [Windows Controls], _win32_Button_GetTextMargin, _win32_Button_GetTextMargin_cpp, commctrl/Button_GetTextMargin, controls.Button_GetTextMargin, controls._win32_Button_GetTextMargin
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Button_GetTextMargin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_GetTextMargin macro


## -description


Gets the margins used to draw text in a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775971(v=VS.85).aspx">BCM_GETTEXTMARGIN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param pmargin

Type: <b>RECT*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the margins to use for drawing text in a button control. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.</div>
<div> </div>


