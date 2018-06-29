---
UID: NF:commctrl.Button_GetSplitInfo
title: Button_GetSplitInfo macro
author: windows-sdk-content
description: Gets information for a specified split button control. Use this macro or send the BCM_GETSPLITINFO message explicitly.
old-location: controls\Button_GetSplitInfo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getsplitinfo.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Button_GetSplitInfo, Button_GetSplitInfo macro [Windows Controls], _shell_Button_GetSplitInfo, _shell_Button_GetSplitInfo_cpp, commctrl/Button_GetSplitInfo, controls.Button_GetSplitInfo, controls._shell_Button_GetSplitInfo
ms.prod: windows
ms.technology: windows-sdk
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
 - Button_GetSplitInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Button_GetSplitInfo macro


## -description


Gets information for a specified split button control. Use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775969(v=VS.85).aspx">BCM_GETSPLITINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param pInfo [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb775955(v=VS.85).aspx">BUTTON_SPLITINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/Bb775955(v=VS.85).aspx">BUTTON_SPLITINFO</a> structure to receive information on the button specified by <i>hwnd</i>. The calling application is responsible for allocating the memory for the structure. Set the <b>mask</b> member of this structure to determine what information to receive.


## -remarks



Use this macro only with the <a href="https://msdn.microsoft.com/library/Bb775951(v=VS.85).aspx">BS_SPLITBUTTON</a> and <a href="https://msdn.microsoft.com/library/Bb775951(v=VS.85).aspx">BS_DEFSPLITBUTTON</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb775951(v=VS.85).aspx">Button Styles</a>



<a href="https://msdn.microsoft.com/library/Bb775947(v=VS.85).aspx">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

