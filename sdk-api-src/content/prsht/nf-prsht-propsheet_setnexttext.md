---
UID: NF:prsht.PropSheet_SetNextText
title: PropSheet_SetNextText macro
author: windows-sdk-content
description: Sets the text of the Next button in a wizard. You can use this macro or send the PSM_SETNEXTTEXT message explicitly.
old-location: controls\PropSheet_SetNextText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setnexttext.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PropSheet_SetNextText, PropSheet_SetNextText macro [Windows Controls], _shell_PropSheet_SetNextText, _shell_PropSheet_SetNextText_cpp, controls.PropSheet_SetNextText, controls._shell_PropSheet_SetNextText, prsht/PropSheet_SetNextText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: prsht.h
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
 - PropSheet_SetNextText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropSheet_SetNextText macro


## -description


Sets the text of the <b>Next</b> button in a wizard. You can use this macro or send the <a href="https://msdn.microsoft.com/4608425e-1724-4d0b-b0f6-9fec147a85f6">PSM_SETNEXTTEXT</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard.


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to a buffer that contains the text.

