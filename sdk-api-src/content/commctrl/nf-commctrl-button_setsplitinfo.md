---
UID: NF:commctrl.Button_SetSplitInfo
title: Button_SetSplitInfo macro
author: windows-sdk-content
description: Sets information for a specified split button control. Use this macro or send the BCM_SETSPLITINFO message explicitly.
old-location: controls\Button_SetSplitInfo.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setsplitinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Button_SetSplitInfo, Button_SetSplitInfo macro [Windows Controls], _shell_Button_SetSplitInfo, _shell_Button_SetSplitInfo_cpp, commctrl/Button_SetSplitInfo, controls.Button_SetSplitInfo, controls._shell_Button_SetSplitInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Button_SetSplitInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_SetSplitInfo macro


## -description


Sets information for a specified split button control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775981(v=VS.85).aspx">BCM_SETSPLITINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param pInfo [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775955(v=VS.85).aspx">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb775955(v=VS.85).aspx">BUTTON_SPLITINFO</a> structure. The calling application is responsible for allocating the memory for this structure and initializing it. Set the <b>mask</b> member of this structure to determine what information to set for the button specified by <i>hwnd</i>. 


## -remarks



Use this macro only with the <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_SPLITBUTTON</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_DEFSPLITBUTTON</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">Button Styles</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb775947(v=VS.85).aspx">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

