---
UID: NF:commctrl.Button_SetTextMargin
title: Button_SetTextMargin macro
author: windows-driver-content
description: Sets the margins for drawing text in a button control. You can use this macro or send the BCM_SETTEXTMARGIN message explicitly.
old-location: controls\Button_SetTextMargin.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_settextmargin.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: Button_SetTextMargin, Button_SetTextMargin macro [Windows Controls], _win32_Button_SetTextMargin, _win32_Button_SetTextMargin_cpp, commctrl/Button_SetTextMargin, controls.Button_SetTextMargin, controls._win32_Button_SetTextMargin
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
-	Button_SetTextMargin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_SetTextMargin macro


## -description


Sets the margins for drawing text in a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/0798b1c5-7db4-46c6-8881-4c847abc7460">BCM_SETTEXTMARGIN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param pmargin

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the margins to set for drawing text in a button control. 


## -remarks




		To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.



