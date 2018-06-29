---
UID: NF:prsht.PropSheet_UnChanged
title: PropSheet_UnChanged macro
author: windows-sdk-content
description: Informs a property sheet that information in a page has reverted to the previously saved state. You can use this macro or send the PSM_UNCHANGED message explicitly.
old-location: controls\PropSheet_UnChanged.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_unchanged.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PropSheet_UnChanged, PropSheet_UnChanged macro [Windows Controls], _win32_PropSheet_UnChanged, _win32_PropSheet_UnChanged_cpp, controls.PropSheet_UnChanged, controls._win32_PropSheet_UnChanged, prsht/PropSheet_UnChanged
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
 - PropSheet_UnChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_UnChanged macro


## -description


Informs a property sheet that information in a page has reverted to the previously saved state. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774632(v=VS.85).aspx">PSM_UNCHANGED</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hwnd

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


#### - hwndPage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the page that has reverted to the previously saved state.


## -remarks



The property sheet disables the <b>Apply Now</b> button if no other pages have registered changes with the property sheet.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>


