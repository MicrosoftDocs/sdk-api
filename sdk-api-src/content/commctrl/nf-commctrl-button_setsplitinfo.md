---
UID: NF:commctrl.Button_SetSplitInfo
title: Button_SetSplitInfo macro
author: windows-driver-content
description: Sets information for a specified split button control. Use this macro or send the BCM_SETSPLITINFO message explicitly.
old-location: controls\Button_SetSplitInfo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setsplitinfo.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: Button_SetSplitInfo, Button_SetSplitInfo macro [Windows Controls], _shell_Button_SetSplitInfo, _shell_Button_SetSplitInfo_cpp, commctrl/Button_SetSplitInfo, controls.Button_SetSplitInfo, controls._shell_Button_SetSplitInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Button_SetSplitInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_SetSplitInfo macro


## -description


Sets information for a specified split button control. Use this macro or send the <a href="https://msdn.microsoft.com/609b8972-9616-4850-a72c-2f87ce19f563">BCM_SETSPLITINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param pInfo [in]

Type: <b><a href="https://msdn.microsoft.com/ea2292c3-1dad-4e4f-9ebc-1719c86848c6">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ea2292c3-1dad-4e4f-9ebc-1719c86848c6">BUTTON_SPLITINFO</a> structure. The calling application is responsible for allocating the memory for this structure and initializing it. Set the <b>mask</b> member of this structure to determine what information to set for the button specified by <i>hwnd</i>. 


## -remarks



Use this macro only with the <a href="Button_Styles.htm">BS_SPLITBUTTON</a> and <a href="Button_Styles.htm">BS_DEFSPLITBUTTON</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/30254cb5-43cd-407f-8ad6-bd7f9ec3edc7">Button Styles</a>



<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

