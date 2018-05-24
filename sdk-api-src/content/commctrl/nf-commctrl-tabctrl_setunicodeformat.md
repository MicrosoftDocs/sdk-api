---
UID: NF:commctrl.TabCtrl_SetUnicodeFormat
title: TabCtrl_SetUnicodeFormat macro
author: windows-driver-content
description: Sets the Unicode character format flag for the control.
old-location: controls\TabCtrl_SetUnicodeFormat.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_setunicodeformat.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: TabCtrl_SetUnicodeFormat, TabCtrl_SetUnicodeFormat macro [Windows Controls], _win32_TabCtrl_SetUnicodeFormat, _win32_TabCtrl_SetUnicodeFormat_cpp, commctrl/TabCtrl_SetUnicodeFormat, controls.TabCtrl_SetUnicodeFormat, controls._win32_TabCtrl_SetUnicodeFormat
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
-	TabCtrl_SetUnicodeFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_SetUnicodeFormat macro


## -description


Sets the Unicode character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/4a9bacfc-d1b7-432a-9b61-b0fe18576679">TCM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/2750b27d-e4a7-416e-b76f-53c26baba399">TabCtrl_GetUnicodeFormat</a>
 

 

