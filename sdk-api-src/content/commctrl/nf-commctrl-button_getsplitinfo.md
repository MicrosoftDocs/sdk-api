---
UID: NF:commctrl.Button_GetSplitInfo
title: Button_GetSplitInfo macro (commctrl.h)
description: Gets information for a specified split button control. Use this macro or send the BCM_GETSPLITINFO message explicitly.
helpviewer_keywords: ["Button_GetSplitInfo","Button_GetSplitInfo macro [Windows Controls]","_shell_Button_GetSplitInfo","_shell_Button_GetSplitInfo_cpp","commctrl/Button_GetSplitInfo","controls.Button_GetSplitInfo","controls._shell_Button_GetSplitInfo"]
old-location: controls\Button_GetSplitInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getsplitinfo.htm
ms.date: 12/05/2018
ms.keywords: Button_GetSplitInfo, Button_GetSplitInfo macro [Windows Controls], _shell_Button_GetSplitInfo, _shell_Button_GetSplitInfo_cpp, commctrl/Button_GetSplitInfo, controls.Button_GetSplitInfo, controls._shell_Button_GetSplitInfo
f1_keywords:
- commctrl/Button_GetSplitInfo
dev_langs:
- c++
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
- Button_GetSplitInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_GetSplitInfo macro


## -description


Gets information for a specified split button control. Use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-getsplitinfo">BCM_GETSPLITINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.


### -param pInfo [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-button_splitinfo">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-button_splitinfo">BUTTON_SPLITINFO</a> structure to receive information on the button specified by <i>hwnd</i>. The calling application is responsible for allocating the memory for the structure. Set the <b>mask</b> member of this structure to determine what information to receive.


## -remarks



Use this macro only with the <a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">BS_SPLITBUTTON</a> and <a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">BS_DEFSPLITBUTTON</a> button styles.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/button-styles">Button Styles</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/button-types-and-styles">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

