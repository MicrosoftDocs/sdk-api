---
UID: NF:prsht.PropSheet_GetTabControl
title: PropSheet_GetTabControl macro
author: windows-sdk-content
description: Retrieves the handle to the tab control of a property sheet. You can use this macro or send the PSM_GETTABCONTROL message explicitly.
old-location: controls\PropSheet_GetTabControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_gettabcontrol.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropSheet_GetTabControl, PropSheet_GetTabControl macro [Windows Controls], _win32_PropSheet_GetTabControl, _win32_PropSheet_GetTabControl_cpp, controls.PropSheet_GetTabControl, controls._win32_PropSheet_GetTabControl, prsht/PropSheet_GetTabControl
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_GetTabControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_GetTabControl macro


## -description


Retrieves the handle to the tab control of a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774580(v=VS.85).aspx">PSM_GETTABCONTROL</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>


