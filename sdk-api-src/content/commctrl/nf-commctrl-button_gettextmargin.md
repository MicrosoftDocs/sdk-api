---
UID: NF:commctrl.Button_GetTextMargin
title: Button_GetTextMargin macro (commctrl.h)
description: Gets the margins used to draw text in a button control. You can use this macro or send the BCM_GETTEXTMARGIN message explicitly.
helpviewer_keywords: ["Button_GetTextMargin","Button_GetTextMargin macro [Windows Controls]","_win32_Button_GetTextMargin","_win32_Button_GetTextMargin_cpp","commctrl/Button_GetTextMargin","controls.Button_GetTextMargin","controls._win32_Button_GetTextMargin"]
old-location: controls\Button_GetTextMargin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_gettextmargin.htm
ms.date: 12/05/2018
ms.keywords: Button_GetTextMargin, Button_GetTextMargin macro [Windows Controls], _win32_Button_GetTextMargin, _win32_Button_GetTextMargin_cpp, commctrl/Button_GetTextMargin, controls.Button_GetTextMargin, controls._win32_Button_GetTextMargin
f1_keywords:
- commctrl/Button_GetTextMargin
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
- Button_GetTextMargin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_GetTextMargin macro


## -description


Gets the margins used to draw text in a button control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-gettextmargin">BCM_GETTEXTMARGIN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control. 


### -param pmargin

Type: <b>RECT*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the margins to use for drawing text in a button control. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>


