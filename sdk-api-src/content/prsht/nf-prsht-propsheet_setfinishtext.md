---
UID: NF:prsht.PropSheet_SetFinishText
title: PropSheet_SetFinishText macro
author: windows-sdk-content
description: Sets the text of the Finish button in a wizard, shows and enables the button, and hides the Next and Back buttons. You can use this macro or send the PSM_SETFINISHTEXT message explicitly.
old-location: controls\PropSheet_SetFinishText.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setfinishtext.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: PropSheet_SetFinishText, PropSheet_SetFinishText macro [Windows Controls], _win32_PropSheet_SetFinishText, _win32_PropSheet_SetFinishText_cpp, controls.PropSheet_SetFinishText, controls._win32_PropSheet_SetFinishText, prsht/PropSheet_SetFinishText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: prsht.h
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_SetFinishText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_SetFinishText macro


## -description


Sets the text of the Finish button in a wizard, shows and enables the button, and hides the Next and Back buttons. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774615(v=VS.85).aspx">PSM_SETFINISHTEXT</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to the new text for the Finish button.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Window handle (HWND) of the wizard property sheet.


## -remarks



By default, the Finish button does not have a keyboard accelerator. You can create a keyboard accelerator with this macro by including an ampersand (&amp;) in the text string that you assign to <i>lpszText</i>. For example, "&amp;Finish" defines F as the accelerator key.



