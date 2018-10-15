---
UID: NF:prsht.PropSheet_SetHeaderSubTitle
title: PropSheet_SetHeaderSubTitle macro
author: windows-sdk-content
description: Sets the subtitle text for the header of a wizard's interior page. You can use this macro or send the PSM_SETHEADERSUBTITLE message explicitly.
old-location: controls\PropSheet_SetHeaderSubTitle.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setheadersubtitle.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PropSheet_SetHeaderSubTitle, PropSheet_SetHeaderSubTitle macro [Windows Controls], _win32_PropSheet_SetHeaderSubTitle, _win32_PropSheet_SetHeaderSubTitle_cpp, controls.PropSheet_SetHeaderSubTitle, controls._win32_PropSheet_SetHeaderSubTitle, prsht/PropSheet_SetHeaderSubTitle
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
 - PropSheet_SetHeaderSubTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_SetHeaderSubTitle macro


## -description


Sets the subtitle text for the header of a wizard's interior page. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774621(v=VS.85).aspx">PSM_SETHEADERSUBTITLE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard's window.


### -param index

Type: <b>int</b>

Zero-based index of the page.


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

New header subtitle.


## -remarks



If you specify the current page, it will immediately be repainted to display the new subtitle.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774651(v=VS.85).aspx">PropSheet_HwndToIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774653(v=VS.85).aspx">PropSheet_IdToIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774664(v=VS.85).aspx">PropSheet_PageToIndex</a>



<b>Reference</b>
 

 

