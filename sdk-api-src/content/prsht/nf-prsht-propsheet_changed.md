---
UID: NF:prsht.PropSheet_Changed
title: PropSheet_Changed macro
author: windows-sdk-content
description: Informs a property sheet that information in a page has changed. You can use this macro or send the PSM_CHANGED message explicitly.
old-location: controls\PropSheet_Changed.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_changed.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropSheet_Changed, PropSheet_Changed macro [Windows Controls], _win32_PropSheet_Changed, _win32_PropSheet_Changed_cpp, controls.PropSheet_Changed, controls._win32_PropSheet_Changed, prsht/PropSheet_Changed
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PropSheet_Changed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_Changed macro


## -description


Informs a property sheet that information in a page has changed. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774576(v=VS.85).aspx">PSM_CHANGED</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the page that has changed.


## -remarks



The property sheet enables the <b>Apply</b> button.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>


